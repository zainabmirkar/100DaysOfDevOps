# Elastic Load Balancer

1) Elastic Load Balancing automatically distributes your incoming traffic across multiple targets, such as EC2 instances, containers, and IP addresses,
in one or more Availability Zones. It monitors the health of its registered targets, and routes traffic only to the healthy targets.
Elastic Load Balancing scales your load balancer capacity automatically in response to changes in incoming traffic.
2) It handle the load of your application across single or multiple az.
3) Elastic Load Balancing supports the following load balancers: Application Load Balancers, Network Load Balancers, Gateway Load Balancers, and Classic Load Balancers.
4) automatically meet user's demands by sutoscaling i.e scaling in and scaling out.
5) you get a dns name that you can bind with security group.
6) monitor your applications and their performance in real time with amazon cloudwatch metrics, logging, request tracing etc.
7) you can configure stickiness. (not sure if I understand this point)

# Why you should use ec2 load balancers?
1) AWS managed
2) reduces cost
3) load balancers are intergrated with other services as well like RDS, SNS, VPC, Route 53, Amazon AMI etc.


# Types of Load Balancers:

1) Network Load Balancers(2017)
 - It works over tcp, udp and tls. Maintains ultra low latency. operates on layer 4

2) Application Load Balancers(2016)
 - load balancing of http and https traffic. For microservices and container based applications. operates on layer 7

3) Classic Load Balancers (2009)
 - old generation not recommended.
 
 
 # Health checks in Load Balancing
 
 - uses active and passive health checks.
 ## Active
  load balancer periodically sends a request to each registered target to check its status.
 - after that it closes the connection that was made established for health check.
 ## Passive
 - Load balancer observeshow targets respond to connections.
 - enables the LB to detect unhealthy targets before it is reported unhealthy by active checks.
 - Health checks are done on url routes or ports. Expects 200 response to term it as healthy. 

## Listener
 - It is a process/rule that checks for connection requests, using the protocol and port that you have configure.
