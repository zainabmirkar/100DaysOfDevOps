# S3 STORAGE CLASSES
- Each object in Amazon S3 has a storage class associated with it.
-  You choose a class depending on your use case scenario and performance access requirements. 

# Storage classes for frequently accessed objects
# S3 Standard
- The default storage class. If you don't specify the storage class when you upload an object, Amazon S3 assigns the S3 Standard storage class. expensive storage.
- Designed for frequently accessed data (more than once a month) with millisecond access
- Durability is 99.999999999%
- Availability (designed for) 99.99%
- Availability Zones >= 3
- support ssl for data-in-transit and encryption of data in rest.
- storage cost is high but very less charge for accessing the objects.
- Largest object that can be uploaded in a single put is 5gb. <br/>


# S3 Standard-IA
![image](https://user-images.githubusercontent.com/85761276/199428601-2bd0dfd8-f32d-412f-a997-7ae857e3bcbb.png)

# AMAZON ONE-ZONE IA
- Recreatable, infrequently accessed data (once a month) with millisecond access
- Min storage duration 30 days
- Per GB retrieval fees apply. Not resilient to the loss of the Availability Zone.
 
![image](https://user-images.githubusercontent.com/85761276/199488598-6dae0ff3-4911-4521-a52e-5e4e37b785fb.png)


# S3 INTELLIGENT TIERING
![image](https://user-images.githubusercontent.com/85761276/199429901-8fc4ba10-4b04-4ff9-81ad-add090de9c41.png)
- Data with unknown, changing, or unpredictable access patterns.
- Monitoring and automation fees per object apply. No retrieval fees.

# AMAZON S3 GLACIER
  ![image](https://user-images.githubusercontent.com/85761276/199489526-bd8bc136-187f-433a-949e-7075238c82f8.png) <br/>



References : [Read in detail](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html)
