# Load Balancing

scalability: meet requirements by changing scale and size.
two types :1) Horizontal scalability: adding multiple systems to your rescue. Adding additional instance and balance the load by adding load balancers.
Used for microservices/distributed applications.
Scaling out: adding more instances if the demand increases. 
Scaling in: Removing the instances if the demand decreases.


2)Vertical scalability: It is the property to increase the capacity of a machine/system by adding more processing power like increasing storage, cpu, memory and other resources.
In aws terma increasing the capacity of your instance.
Increase capacity means scaling up else scaling down. upgrading from t2.micro to t2.large. 
Used for non distributed systems like databases.


# High Availabillity in AWS: 
1) Having the ability to make your application available to the user.
2) hIGH AVAILABILITY IS ON THE LINES OF HORIZONTAL scaling.
3) make it more available by having them hosted across multiple az.
4) The users will still be able to access the websiteeven if one or two data centres went down.
5) Use availability zone load balancer and auto scaling group.


# Difference between high availability and scalability
in vertical scaling there is a single point of failure. that's why we have availability concept.

