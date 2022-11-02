# SIMPLE STORAGE SERVICE


![image](https://user-images.githubusercontent.com/85761276/198949065-43fa770e-3e0c-4af9-9ac9-bd0b57482f7a.png)
- Bucket ownership is non transferable
- cannot create nested bucket
- region specific
- 100 buckets per account but can request aws for more.

# S3 BUCKET NAMING RULES

![image](https://user-images.githubusercontent.com/85761276/198949679-79778a66-23ac-4ba4-b295-ef107d961876.png)
![image](https://user-images.githubusercontent.com/85761276/198949742-00610948-9059-4ee5-a988-889a77ef348d.png)


- Bucket name must be a series of one or more lables (xyz.index)

# S3 BUCKET SUBRESOURCES
![image](https://user-images.githubusercontent.com/85761276/198950278-358fcb0f-61c0-4a9e-8323-ceee1c5ff65a.png)
![image](https://user-images.githubusercontent.com/85761276/198952815-c666a381-2703-4763-8956-83d01da24092.png)

- cannot disable versioning.
- acl for who can access your bucket.


# S3 OBJECTS
![image](https://user-images.githubusercontent.com/85761276/198953000-84647bd0-c66a-4d61-8985-d31e55b0a260.png)
![image](https://user-images.githubusercontent.com/85761276/198953119-80708a43-5b06-4ff9-b239-880f506b126d.png)


# S3 VERSIONING

- Versioning-enabled buckets can help you recover objects from accidental deletion or overwrite. 
- For example, if you delete an object, Amazon S3 inserts a delete marker instead of removing the object permanently. 
- The delete marker becomes the current object version. 
- If you overwrite an object, it results in a new object version in the bucket. You can always restore the previous version. 
- Buckets can be in one of three states:Unversioned (the default), Versioning-enabled and Versioning-suspended.
- You enable and suspend versioning at the bucket level. After you version-enable a bucket, it can never return to an unversioned state. But you can suspend versioning on that bucket.
- The versioning state applies to all (never some) of the objects in that bucket.
-  When you enable versioning in a bucket, all new objects are versioned and given a unique version ID.
-  Objects that already existed in the bucket at the time versioning was enabled will thereafter always be versioned and given a unique version ID when they are       modified by future requests. 
-  Objects that are stored in your bucket before you set the versioning state have a version ID of null. 
-  The bucket owner (or any user with appropriate permissions) can suspend versioning to stop accruing object versions. 
-  When you suspend versioning, existing objects in your bucket do not change. 
-  object deletion in a suspended versioning bucket, will only delete the objects with id "null".
-  To customize your data retention approach and control storage costs, use object versioning with S3 Lifecycle. [Managing your storage lifecycle](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html)
-  These actions define when objects transition to another storage class. For example, you might choose to transition objects to the S3 Standard-IA storage class 30 days after creating them, or archive objects to the S3 Glacier Flexible Retrieval storage class one year after creating them

# MFA DELETE

![image](https://user-images.githubusercontent.com/85761276/199411955-baef6a7e-bf01-44de-930c-af04dcecd453.png)
![image](https://user-images.githubusercontent.com/85761276/199412126-b8951cbd-c63c-4bdd-bebf-9260b1b43829.png)



# MULTIPART UPLOAD
- used to upload object in parts.
- using the aws sdk's (high level api). You can upload data from a file or a stream. You can also set advanced options, such as the part size you want to use for the multipart upload, or the number of concurrent threads you want to use when uploading the parts. You can also set optional object properties, the storage class, or the access control list (ACL).
- If you need to pause and resume multipart uploads, vary part sizes during the upload, or do not know the size of the data in advance, use the low-level PHP API.<br/>

 https://docs.aws.amazon.com/AmazonS3/latest/userguide/mpu-upload-object.html


# COPYING S3 OBJECTS
![image](https://user-images.githubusercontent.com/85761276/199414257-193753e7-fa51-4ef2-adbc-e03652180c1d.png)
![image](https://user-images.githubusercontent.com/85761276/199414385-c2542038-a624-49f1-9288-968aff624f28.png)
- system metadata which you cannot change.
- user metadata <br/>




<br/>


References <br/>
https://www.youtube.com/watch?v=IHnorot0kxM&list=PLBGx66SQNZ8a_y_CMLHchyHz_R6-6i-i_&index=31 <br/>
https://www.youtube.com/watch?v=S_RV_NTABo0&list=PLBGx66SQNZ8a_y_CMLHchyHz_R6-6i-i_&index=32
  

