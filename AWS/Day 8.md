# Auto Scaling Groups 

AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost. <br/>

Scaling out : adding more ec2 instances to meet the growong demand
Scaling in: decreasing ec2 instances when you don't need them

![image](https://user-images.githubusercontent.com/85761276/198017545-3c84a949-edca-413b-aa81-eea36e5a46f0.png)

<br/>

# ASG with load balancers

![image](https://user-images.githubusercontent.com/85761276/198017875-c9fef63f-9e21-481c-bce8-8c11e617e30a.png)

<br/>
- when load increases asg adds two more instances <br/>
- those instances automatically gets registered in the load balancer target group<br/><br/>



# Creating asg
![image](https://user-images.githubusercontent.com/85761276/198018353-d779f637-2e54-49c1-9352-c56ae5ec76ff.png)

What is a fleet in AWS? <br/>
An EC2 Fleet is a group of On-Demand Instances and Spot Instances. The EC2 Fleet attempts to launch the number of instances that are required to meet the target capacity that you specify in the fleet request.

When to scale? <br/>
By using target tracking we will tell the asg when the cpu utilization goes up by a certain percentage to scale up or down. <br/>


# Autoscaling strategies
- manual scaling
- dynamic scaling
- predictive scaling using ml 



















references: <br/>
https://www.youtube.com/watch?v=NGWKbF67_1Q&list=PLiH9_MU-6RjI9gdFqmvUfKRfw_zRxIb6o&index=15
