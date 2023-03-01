# NAT Gateways
- A NAT gateway is a Network Address Translation (NAT) service. 
- You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances. <br/>
  ![image](https://user-images.githubusercontent.com/85761276/218319651-89a415c4-1e11-4ca7-b2de-475cde5f5907.png)





- NAT gateways and NAT instances are both used for the one purpose. And that purpose is to enable the instances that we deploy into private subnets to connect to the internet.

- This is outbound only. It doesn't mean there's going to be bi-directional traffic. If we wanted that, we would just deploy our instances into a public subnet and they would have a public
IP and use the internet gateway.

- But sometimes we want private instances, so no one in the outside world from the internet can connect to our EC2 instance, but we can connect outbound.

- We might want to be able to connect to an outbound service, a service located on the internet, or we might want to download software, software updates, that kind of thing.
- So again, we have an availability zone with a public subnet and a private subnet. And we've deployed in EC2 instance in a private subnet d it has a private IP address. And there's an internet gateway attached to the VPC.
What we might then do is deploy a NAT gateway into a public subnet.

- Now it's important to understand that this NAT gateway is in a public subnet because it needs a public IP address.

- It will have an elastic IP address assigned to it, and it uses that to be able to talk to the internet gateway on behalf of our private instance.

- ```You always deploy your NAT gateways or your NAT instances in public subnets.```

- So we then have our route tables. As you know, the route table for the public subnet, the main route table has a route to the internet gateway.

- But we also have a private route table. And in this case, we have added an entry. And that entry is for the NAT gateway ID of this NAT gateway we've deployed.

- And just like with the internet gateway entry here, it's 0.0.0.0/0. So it means any address other than this address here that's already been specified.

- So any address range outside of the VPC. With this configuration, our EC2 instance can now use its private IP address to connect to the private IP address of the NAT gateway,
and then traffic can get forwarded to the internet gateway from the NAT gateway using Network Address

- And from there, it would go out to the internet to whatever service you want to connect to.

So that's a NAT gateway. A NAT gateway is an AWS service that you can deploy.

- The following is the route table associated with the private subnet in Availability Zone B. The first entry is the local route; it enables the instances in the subnet to communicate with other instances in the VPC using private IP addresses.
-  The second entry sends all other subnet traffic to the NAT gateway. <br/>
 ![image](https://user-images.githubusercontent.com/85761276/218319759-f8917ee0-beca-44b7-91d8-77290e9a55c6.png)
<br/>


# NAT instances
- You can create your own AMI that provides network address translation and use your AMI to launch an EC2 instance as a NAT instance.
- https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-comparison.html

<br/>

# sg vs nacl
- sg can be applied to instance. it works at instance level
- nacl works at subnet level
- sg supports aloow rules only. there is no such tjing as denying a rule
- sg is statefull meaning it allows return traffic.
- nacl is stateless meaning you need to have inbound as well as outbound


 References <br/> 
 https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html <br/>
 https://docs.aws.amazon.com/vpc/latest/userguide/nat-gateway-scenarios.html
