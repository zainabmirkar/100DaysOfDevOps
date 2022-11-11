# Docker Containers and Microservices
- A container includes all the settings, dependencies, code for running the application
- Each container is isolated from other containers.
- Start up very quickly
- Resource efficient. They don't use huge amount of processing power or memory because they dont't have that operating system in each container. They use the underlying os


# Microservices
- Microservices can be containerized with Docker, which reduces application design, serves a single purpose, and exposes an API.
- Using Docker, it is easy to create required services separately and manage them as microservices without affecting other services

# Is docker and microservices same?
- Docker is a Cup or in other words Container whereas Microservice is the liquid that you pour into it. You can pour different types of liquids in the same cup. But it will get crowded. Similarly, you can run many Microservices in same Docker container.



# Amazon ECS
- used for managing containers
- You can use it to run, stop, and manage containers on a cluster.
- With Amazon ECS, your containers are defined in a task definition that you use to run an individual task or task within a service.
- In this context, a service is a configuration that you can use to run and maintain a specified number of tasks simultaneously in a cluster.

# Features
- A serverless option with AWS Fargate. With AWS Fargate, you don't need to manage servers, handle capacity planning, or isolate container workloads for security. 
- Integration with AWS Identity and Access Management (IAM). You can assign granular permissions for each of your containers. 
- AWS managed container orchestration. As a fully managed service, Amazon ECS comes with AWS configuration and operational best practices built-in. This also means that you don't need to manage control plane, nodes, or add-ons. 
- Continuous integration and continuous deployment (CI/CD). This is a common process for microservice architectures that are based on Docker containers. You can create a CI/CD pipeline
- Support for sending your container instance log information to CloudWatch Logs. 

For more features [Read Documentation](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)


# Amazon ECS Components
- An Amazon ECS cluster: It is a logical grouping of tasks or services. You can use clusters to isolate your applications.
- Containers and images: To deploy applications on Amazon ECS, your application components must be configured to run in containers. Images are typically built from a Dockerfile. 

![image](https://user-images.githubusercontent.com/85761276/201280315-1f18e9c5-d025-4fbc-b158-aeb2bbce08f7.png)

- Task definitions: A task definition is a text file that describes one or more containers that form your application. It's in JSON format. You can use it to describe up to a maximum of ten containers. The task definition functions as a blueprint for your application. It specifies the various parameters for your application. 

- Tasks: It is a running docker container using settings in a task definition.
- Services: You can use an Amazon ECS service to run and maintain your desired number of tasks simultaneously in an Amazon ECS cluster. How it works is that, if any of your tasks fail or stop for any reason, the Amazon ECS service scheduler launches another instance based on your task definition. It does this to replace it and thereby maintain your desired number of tasks in the service.
- Container agent: The container agent runs on each container instance within an Amazon ECS cluster.


# ECS Launch types
- There are two models that you can use to run your containers:

- Fargate launch type - This is a serverless pay-as-you-go option. You can run containers without needing to manage your infrastructure. Fargate automatically provision resources, manages compute. Charged for running tasks. efs, handles cluster optimization, limited control. Infrasructure is automated. Small workloads that have occasional burst

- EC2 launch type - Configure and deploy EC2 instances in your cluster to run your containers. Explicitly provision ec2 instances. You are responsible for running ec2 instances. hrged per ec2 instance running. Docker volumes, efs and fsx for windows file server. You handle cluster optimization. More granula control over infrastructure.












