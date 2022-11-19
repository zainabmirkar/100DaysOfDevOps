# Replicating objects
- Replication enables automatic, asynchronous copying of objects across Amazon S3 buckets. 
- Buckets that are configured for object replication can be owned by the same AWS account or by different accounts.
- You can replicate objects to a single destination bucket or to multiple destination buckets. 
- The destination buckets can be in different AWS Regions or within the same Region as the source bucket.
- To automatically replicate new objects as they are written to the bucket use live replication, such as Same-Region Replication (SRR) or Cross-Region Replication (CRR).
- To replicate existing objects to a different bucket on demand, use S3 Batch Replication.

# Why use replication: refer documentation

# When to use Cross-Region Replication

- S3 Cross-Region Replication (CRR) is used to copy objects across Amazon S3 buckets in different AWS Regions. CRR can help you do the following:

- Meet compliance requirements – Although Amazon S3 stores your data across multiple geographically distant Availability Zones by default, compliance requirements might dictate that you store data at even greater distances.
-  To satisfy these requirements, use Cross-Region Replication to replicate data between distant AWS Regions.

- Minimize latency – If your customers are in two geographic locations, you can minimize latency in accessing objects by maintaining object copies in AWS Regions that are geographically closer to your users.

- Increase operational efficiency – If you have compute clusters in two different AWS Regions that analyze the same set of objects, you might choose to maintain object copies in those Regions.


# When to use Same-Region Replication
- Same-Region Replication (SRR) is used to copy objects across Amazon S3 buckets in the same AWS Region. 
- SRR can help you do the following:

- Aggregate logs into a single bucket – If you store logs in multiple buckets or across multiple accounts, you can easily replicate logs into a single, in-Region bucket.
Doing so allows for simpler processing of logs in a single location.

- Configure live replication between production and test accounts – If you or your customers have production and test accounts that use the same data, you can replicate objects between those multiple accounts, while maintaining object metadata.

- Abide by data sovereignty laws – You might be required to store multiple copies of your data in separate AWS accounts within a certain Region. Same-Region Replication can help you automatically replicate critical data when compliance regulations don't allow the data to leave your country.


# Points to remember while replication
- versioning should be enabled
- the objects that are uploaded after replication, only those are replicated and not the earlier objects. However you can choose to replicate the existing objects.
- If you have applied replication rule to bucket1 then the objects in the bucket1 will be replicated to the destination bucket and not vice versa.

# Steps
- Create buckets, after that go to management then add a replication rule.
  ![image](https://user-images.githubusercontent.com/85761276/200109496-db852901-7999-4b1c-806e-271e9bbc7767.png)

- add objects to the bucket
  ![image](https://user-images.githubusercontent.com/85761276/200109546-753a7410-d07f-4844-9927-d91d101f5b73.png)
 
- you can see the objects replicating in destination bucket.

  ![image](https://user-images.githubusercontent.com/85761276/200109587-d68df276-2489-4592-aada-575fdf72564e.png)


References: https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication-walkthrough1.html


