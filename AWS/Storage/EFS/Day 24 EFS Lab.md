# EFS Lab


# Firstly, create two instances in different AZ's within the same region.
https://docs.aws.amazon.com/efs/latest/ug/gs-step-one-create-ec2-resources.html
- When you are creating instances, mention these two security groups.
    ![image](https://user-images.githubusercontent.com/85761276/200592869-b9cc19e7-3a59-4f6b-9aa0-99be33796af4.png)




# Then create a file system with custom settings using the Amazon EFS console

- Step 1: Configure file system settings. open the Amazon EFS console, click on customize. The File system settings page appears. Enter a Name for the file system. Keep the default settings.
- Step 2: Configure network access. You configure the file system's network settings, including the VPC and mount targets.

  ![image](https://user-images.githubusercontent.com/85761276/200584340-aa088dbf-030b-45c7-b824-4d2d0d69b29f.png) <br/>
  For Mount targets, you create one or more mount targets for your file system. The mount target security group acts as a virtual firewall that controls the traffic. For example, it determines which clients can access the file system. For each mount target, set the following properties: AZ, Subnet Id, IP Address, Security groups. 



- Step 3: Create a file system policy (optional)
- Step 4: Review and create



# Mounting on Amazon EC2 Linux instances using the EFS mount helper
1. SSH into your ec2 instances.
    ![image](https://user-images.githubusercontent.com/85761276/200588196-7bfe74d0-386c-4254-baa8-9e0b5f5e2cdd.png)

2. Create a directory efs on both instances that you will use as the file system mount point.
    ![image](https://user-images.githubusercontent.com/85761276/200588392-f73a4c09-31ba-400c-afbf-579e5eba2db9.png)
  
3. Install the amazon-efs-utils package on EC2 instances.
![image](https://user-images.githubusercontent.com/85761276/200588746-d8f0c4fb-78ab-4063-85e0-aa3d49ae034c.png)

4. To display the mount commands to use for this file system, choose Attach. Copy efs mount helper command
    ![image](https://user-images.githubusercontent.com/85761276/200589114-9e0da2c0-bc4b-482d-bfd3-d54d21ddd102.png)

5. If necessary install the botocore dependency. <br/>

6. Run the mount command. 

    ![image](https://user-images.githubusercontent.com/85761276/200589785-50ff502a-0f8a-4d95-a085-d158c75aa4fc.png)

7. Then cd into efs. Create some files using touch command.

    ![image](https://user-images.githubusercontent.com/85761276/200590063-63202a40-979a-4f63-8cfe-c50954d917ce.png)

8. You can see the files created in other instance as well.


    ![image](https://user-images.githubusercontent.com/85761276/200590310-79902ad3-1962-48c4-bbc8-b468fb4cc006.png)


Amazon EC2 and other AWS compute instances running in multiple Availability Zones within the same AWS Region can access the file system, so that many users can access and share a common data source. <br/>

<br/>

References: https://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-helper-ec2-linux.html <br/>
https://docs.aws.amazon.com/efs/latest/ug/creating-using-create-fs.html <br/>
https://docs.aws.amazon.com/efs/latest/ug/accessing-fs-create-security-groups.html












