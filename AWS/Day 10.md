
![image](https://user-images.githubusercontent.com/85761276/198318132-6592d2c3-403f-4f7b-8c7e-435baebf654e.png)


# Format and mount an attached volume
- connect to ec2 instance <br/>
  ![image](https://user-images.githubusercontent.com/85761276/198529516-30c16128-37e3-48ac-b9e8-8bc4b2ada235.png) <br/>
 
- lsblk command to view your available disk devices and their mount points (if applicable) to help you determine the correct device name to use. <br/>
 
  ![image](https://user-images.githubusercontent.com/85761276/198529835-b47d70a1-95e0-47fe-afaa-4135e2b8513c.png) <br/>

-Determine whether there is a file system on the volume. Use the file -s command to get information about a specific device, such as its file system type. If the output shows simply data, as in the following example output, there is no file system on the device <br/>

  ![image](https://user-images.githubusercontent.com/85761276/198530214-66ba3cb8-8272-4a7e-9d59-81906cd50525.png) <br/>

- If the device has a file system, the command shows information about the file system type. For example, the following output shows a root device with the XFS file system. <br/>
- create a file system if not present
  ![image](https://user-images.githubusercontent.com/85761276/198530483-517f1477-e144-4f4d-b853-75466cfeb63e.png) <br/>
  
- Use the mkdir command to create a mount point directory for the volume. sudo mkdir /data. <br/>

- Use the following command to mount the volume at the directory you created in the previous step.
[ec2-user ~]$ sudo mount /dev/xvdf /data  <br/>

  ![image](https://user-images.githubusercontent.com/85761276/198531573-8f76689f-488d-4c37-b930-0108ce94c273.png) <br/>

# Automatically mount an attached volume after reboot

- To mount an attached EBS volume on every system reboot, add an entry for the device to the /etc/fstab file. <br/>
- Create a backup of your /etc/fstab file that you can use if you accidentally destroy or delete this file while editing it.<br/>
  ![image](https://user-images.githubusercontent.com/85761276/198531840-71399581-6359-4b0d-b61d-6e5e6af6adf7.png) <br/>

- Open the /etc/fstab file using any text editor, such as nano or vim. <br/>
[ec2-user ~]$ sudo vim /etc/fstab <br/>

- To verify that your entry works, run the following commands to unmount the device and then mount all file systems in /etc/fstab. If there are no errors, the /etc/fstab file is OK and your file system will mount automatically after it is rebooted. <br/>

   ![image](https://user-images.githubusercontent.com/85761276/198532266-693aedda-7c46-4826-b09b-35af0ff6aca5.png) <br/>



- References <br/>
  https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-using-volumes.html <br/>
  https://www.youtube.com/watch?v=oWMyp1AXtaY


