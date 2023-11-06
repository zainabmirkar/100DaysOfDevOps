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
- endpoints allow you to connect to aws services using a private network instead of a public network
- enhanced security
- low latency
- vpc endpoint gateway (s3 and dynamodb)
- rest of the services it is going to be an interface

## Private Link
- A PrivateLink in AWS allows you to securely access services hosted on AWS privately, without needing to traverse the public internet.
- requires a network loadbalancer and eni (Elastic Network Interface)

## Site to Site VPN and Direct Connect







