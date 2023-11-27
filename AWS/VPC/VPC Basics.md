# VPC Basics
- VPC (private network to deploy your resources)
- regional resource
- IPv6 (3.4X10^38 addresses)

## Subnets
- allows you to partition your network inside your vpc (AZ resource)
- public subnet is accessible from the internet
- private subnet is not accessible from the internet

## Route tables
- A route table is a set of rules, known as routes, that determines how network traffic is directed within your VPC
- When you create a VPC, AWS automatically creates a default route table for that VPC.
- In addition to the default route table, you can create custom route tables to have more control over routing within your VPC
- To enable communication between your VPC and the internet, you can add a route to the IGW in your route table

## Internet gateway
- helps vpc instances connect with the internet
- public subnets have a route to the internet gateway

## Nat gateway
- allows instances in private subnet to access the internet while remaining private
- nat gateway is deployed in public subnet
- then we create a route in private subnet to the nat gateway (which resides in public subnet) and then to the igw
- only accept outbound and not inbound
- managed by awsm

## NACL
- works at subnet level
- a firewall that controls traffic from and to subnet
- by default nacl allows inbound and outbound traffic
- have options for noht allow and deny rules
- stateless

## SG
- works at instance level
- stateful

## VPC Flow logs
- VPC flow logs are a log of all the IP traffic going through your interfaces. So you can get a VPC flow log, a subnet flow log
or even an elastic tech network interface flow log to see the traffic going in and out of your EC2 instances for example.
- By enabling the flow log, we can monitor and troubleshoots for connectivity issues.
- For example, if a subnet cannot connect to the internet, or a subnet cannot connect to another subnet, or the internet cannot access a subnet,
this will be captured by the VPC flow log and we can look at it to get to the root cause of it.
- So this is super important because on top of getting information out of our EC2 instances, we also get information for elastic load balancers, ElastiCache,
RDS, Aurora, et cetera, et cetera.
- And the VPC flow logs can go to S3, CloudWatch Logs, and Kinesis Data Firehose.

## VPC Peering
- connect 2 vpcs privately using aws network
- make them behave as if they are in the same network
- must not have overlapping cidr(ip range)
- connection is not transitive

## VPC Endpoints
- endpoints allow you to connect to aws services using a private network instaed of using virtual private gateway, nat, internet gatewway, vpn or dc
- enhanced security
- low latency
- there are 2 types interface endpoint and gateway endpoint
- In AWS, an interface endpoint is a logical connection between your Virtual Private Cloud (VPC) and a supported AWS service. It allows you to access the AWS service over the Amazon network instead of over the internet. This can enhance security by keeping traffic between your VPC and the AWS service within the AWS network, without going over the public internet.  they use eni's with private ip
- gateway doesn't use eni's. Gateway endpoints do not enable AWS PrivateLink. only work with ipv4
- vpc endpoint gateway (s3 and dynamodb)
- rest of the services it is going to be an interface

## Private Link
- A PrivateLink in AWS allows you to securely access services hosted on AWS privately, without needing to traverse the public internet.
- requires a network loadbalancer and eni (Elastic Network Interface)
- privatelink consists of service providers and service consumers

## Site to Site VPN and Direct Connect


## Bastion host
- ec2 instance sits in public subnet which is bound by sg (TCP 22) sorce will be engineer's ip that need to connect to private server
- private servers will also have to configure sg which matches the sg of bastion server
- ssh agent forwarding in which the private key is stored on the local machine instead of bastion server which makes it easy and secure to connect to private servers

## VPN 
- suppose we want to create connection between our servers in private subnet and on premise servers we can create a vpn connection
- on aws side create a virtual gateway and on premise side customer gateway then initiate a vpn tunnel between the two endpoints
- vpn tunnel can only be initiated from customer gateway and not virtual gateway

## ENI
- logical virtual network cards within your vpc
- Having several ENIs attached to one instance enables an instance to interact on two separate subnets.
- attach to ec2
- can detach and reconnect to another instance 
- PNI is already attached to ec2 by default labelled as eth0
- all the traffic passing thrugh eni can be captured by vpc flow logs
- A single ENI can be attached to multiple EC2 instances, but each instance can only be connected to one ENI. 





