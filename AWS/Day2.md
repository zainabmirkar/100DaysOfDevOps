 You can connect EC2 from the browser as well. Select the EC2 Instance Connect. <br/>
     <img width="328" alt="ec2 in briowser" src="https://user-images.githubusercontent.com/85761276/188303624-d67d6d83-5512-422d-a256-10011fb98f45.png"> <br/>
    
   
   # What are Security Groups?
  1) Virtual firewalls to control outbound and inbound traffic.
  2) Security groups allow all Outbound traffic but restricts Inbound traffic.
  3) Security groups are attached to Region/ VPC
  4) can be attached to multiple instances and multiple instances can have a common security group.
  5) Please create separate Security group for SSH. It will give connection timeout error if you don't specify an Inbound rule for ssh. If you want to allow access to      a port you need to specify it. <br/>
    https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html

  
    An Ipv6 address uses 128 bits as opposed to 32 bits in IPv4.
    IPv4 uses four 1 byte decimal numbers, separated by a dot (i.e. 192.168. 1.1), while IPv6 uses hexadecimal numbers that are separated by colons 
    (i.e. fe80::d4a8:6435:d2d8:d9f3b11). <br/>
  
  # Public and Private IPs
    If you have public IP then anyone can access the information that you are broadcasting.
    
   # Public IPS <br/>
   Initial IP <br/>
   <img width="847" alt="publicipinitial" src="https://user-images.githubusercontent.com/85761276/188304514-369b8cc7-fc6f-4095-8aa1-fcfda72d37bd.png"> <br/>
   
   I have stopped the instance and started it again. As you can see the IP has changed. <br/>
   
   <img width="657" alt="publibipchanged" src="https://user-images.githubusercontent.com/85761276/188304588-9df39072-138b-4519-987a-b9943d047208.png">


  # Elastic IP
 1) public ip gets changed when you start or stop an instance. 
 2) Elastic IP help you have a fixed Public IP address for your instance. when you restart an instance elastic ips won't change.
 3) attached to one instance at a time. <br/>
   <img width="342" alt="elastic" src="https://user-images.githubusercontent.com/85761276/188304965-f386d5fe-30a2-425c-956a-e4e7100e94da.png">

 4) you get charged for elastic ip it is not attached to running instance or it is associated with stopped instance/Unattached network interface. You don't get charged     if it is attached to a running instance.
 5) maximum of 5 eips. <br/>
    https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html


  # User Data
  1) The User data field is located in the Advanced details section of the launch instance wizard.
  2) It used to bootload an instance (preconfigured instructions).
 

  # Set up an Apache Web Server with Php using User data.
  <img width="379" alt="1" src="https://user-images.githubusercontent.com/85761276/188305334-98e6368d-3c03-4145-b9e3-8b89f6ae79dd.png">

   review and launch the instance

  
 <img width="624" alt="2_cannotreach" src="https://user-images.githubusercontent.com/85761276/188305419-8ce4786f-95c6-453b-80e8-f4daeb71caf5.png">
 timeout<br/>
 
 <img width="876" alt="3inbound_added" src="https://user-images.githubusercontent.com/85761276/188305448-52562556-52c7-4ad9-9ba2-501a4086f3b5.png">
<br/>
Now you can see as the inbound rule for http is specified
 <img width="933" alt="4canseephp" src="https://user-images.githubusercontent.com/85761276/188305478-cad621bc-f64b-41f7-9eef-7a96d6b7df69.png">
 <br/>
 add index.html 
 <br/><img width="463" alt="5html" src="https://user-images.githubusercontent.com/85761276/188305613-86fab828-38bd-4097-a3f9-c4cbe5f222b8.png">

 <br/>

   
  <img width="527" alt="helloworld" src="https://user-images.githubusercontent.com/85761276/188305672-a11c198d-d9fa-4018-9b4f-e0831c41c4e5.png">
  
  References:<br/>
  https://www.youtube.com/watch?v=s3G4p0CLG20&list=PLiH9_MU-6RjI9gdFqmvUfKRfw_zRxIb6o&index=11
  

