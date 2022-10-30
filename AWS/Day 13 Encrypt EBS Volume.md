# EBS ENCRYPTION
![image](https://user-images.githubusercontent.com/85761276/198881485-5ce1f89c-6d03-4043-afb3-4ec7d60facd2.png) <br/>

![image](https://user-images.githubusercontent.com/85761276/198817333-28e1e63e-0902-4edc-b425-03e1eaee8460.png) <br/>
![image](https://user-images.githubusercontent.com/85761276/198817412-2d5f2146-139a-439a-887c-128a081404e1.png) <br/>

- Encryption happens at ec2 side and not on ebs. <br/>

![image](https://user-images.githubusercontent.com/85761276/198817787-9f544073-b40d-478d-99ab-9be0ef4fc2e1.png) <br/>


# One way to encrypt data in ebs (non root volume) <br/>
![image](https://user-images.githubusercontent.com/85761276/198817831-f676b92a-a637-433d-b015-db061c59dfc3.png)





# Second way to encrypt data in ebs (non root volume) <br/>
![image](https://user-images.githubusercontent.com/85761276/198818027-e409fa2c-a59f-4b60-aeef-8b2e7415c379.png)



# Root Volume Encryption <br/>
- Earlier there was no way to encrypt root volume. <br/>
![image](https://user-images.githubusercontent.com/85761276/198818177-b9691fe5-d668-4fb4-9d41-b0e8d8134389.png)

# Instance store <br/>

![image](https://user-images.githubusercontent.com/85761276/198881785-3f25edc6-3ec3-4474-92a6-c26807accb98.png) <br/>

# Share Snapshots
- To encrypt a snapshot or a volume you need a key which is called Customer Masters Key (CMK) and are managed by KMS.
- When encrypting first ebs volume, AWS KMS creates a default CMK key. After that the snapshots, volumes that you will create will be from same key.
- After that each newly encrypted volume is encrypted with a unique/seperate aes-256 bit encryption key. <br/>

  ![image](https://user-images.githubusercontent.com/85761276/198883629-8c9449b3-05fd-4ddd-98c7-edd61ea7d0dd.png) 
  
  ![image](https://user-images.githubusercontent.com/85761276/198883905-50ca11a5-e9d2-47fb-8d44-6fe1c5463d7a.png) 
  
  ![image](https://user-images.githubusercontent.com/85761276/198883970-4d43a1b3-fb98-4b2c-b3c7-bcea506b1036.png)


  ![image](https://user-images.githubusercontent.com/85761276/198884140-001d5ced-996d-40ea-b164-cf6fe4a5e3be.png)
  
  ![image](https://user-images.githubusercontent.com/85761276/198884182-1dc19337-653d-49e8-a22f-bcc7b553f9eb.png)
  
  ![image](https://user-images.githubusercontent.com/85761276/198884411-9f635368-d734-447d-978f-2fffa20d8ee1.png)






- References <br/>
  https://www.youtube.com/watch?v=fUY3NcpJ9sk&list=PLBGx66SQNZ8a_y_CMLHchyHz_R6-6i-i_&index=46 <br/>
  https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html <br/>
  https://www.youtube.com/watch?v=5_E7ureQ0qE&t=3s <br/>
  https://www.youtube.com/watch?v=PIs_B8M00lE&list=PLBGx66SQNZ8a_y_CMLHchyHz_R6-6i-i_&index=47
