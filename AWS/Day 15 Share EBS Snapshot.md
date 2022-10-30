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
