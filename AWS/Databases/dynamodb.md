# DynamoDB 

- nosql database
- single digit millisecond latency
- distributed serverless database
- key value database

### Dynamodb accelerator
- in memory cache ( In-memory caching helps mitigate this latency by keeping a copy of frequently accessed data in a faster memory layer.)
- integrated with dynamodb
- from milliseconds to microsecind latency
- when you go to the console, you will create a table directly and not database because database is already present serverless


### dynamodb global tables
- Global Tables enables automatic multi-region replication of DynamoDB tables, allowing you to have a globally distributed, highly available, and low-latency database solution.
-  When creating a Global Table, you select a primary region where you create the table.
-  After creating the Global Table in the primary region, DynamoDB automatically creates replicas of the table in the secondary regions you specify. Each region has its own replica of the table.
- When a write operation is performed in the primary region, DynamoDB propagates the write to all the replicas before acknowledging the write to the application.
 
















