# Amazon EFS: How it works

- Amazon EFS provides a simple, serverless, set-and-forget elastic file system.
- With Amazon EFS, you can create a file system, mount the file system on an Amazon EC2 instance, and then read and write data to and from your file system. 
- You can mount an Amazon EFS file system in your virtual private cloud (VPC), through the Network File System versions 4.0 and 4.1 (NFSv4) protocol.
- Amazon EC2 and other AWS compute instances running in multiple Availability Zones within the same AWS Region can access the file system, so that many users can access and share a common data source.
- file level storage
- nfs cient should be installed
- can only be used with ec2 instances
- can only be accessed from on-premise servers only using direct connect
- data can grow to petabyte scale
- Data is stored in multiple az's in the same region for high availability.

# What are mount targets?
- A mount target provides an IP address for an NFSv4 endpoint at which you can mount an Amazon EFS file system. 
- You mount your file system using its Domain Name Service (DNS) name, which resolves to the IP address of the EFS mount target in the same Availability Zone as your EC2 instance.
-  You can create one mount target in each Availability Zone in an AWS Region.
-  If there are multiple subnets in an Availability Zone in your VPC, you create a mount target in one of the subnets. 
-  Then all EC2 instances in that Availability Zone share that mount target.
-  Mount targets themselves are designed to be highly available.






References: https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html#how-it-works-conceptual <br/>
https://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-helper-ec2-mac.html <br/>
https://www.youtube.com/watch?v=rsU-UnAtgBM
 
