# Create a cluster

- Open the Amazon ECS console
- On the Clusters page, choose Create Cluster.
- For Select cluster compatibility, choose EC2 Linux + Networking.
- On the Configure cluster page, enter a Cluster name. 
- In the Networking section, configure the VPC for your cluster. You can keep the default settings
- Choose Create.

[Documentation](https://docs.aws.amazon.com/AmazonECS/latest/userguide/create_cluster.html)


# Create new Task Definition
- In the navigation pane, choose task definitions, Create new task definition.
- On the Select launch type compatibilities page, select ec2
- Enter a name for task
- Add Container, fill out each required field and any optional fields to use in your container definitions. I have kept the default settings. For hard limit keep 300, host port 0 and container port 80, cpu units 300 then add.
- Create 


# Create a service
- write name for the service
- launch type ec2
- keep the default settings
- service type replica and number of tasks 2
- Task placement AZ Balance spread.
- Next step will be load balancer select alb.
- Iam role AWSServiceRoleForEcs
- Create a load balancer
