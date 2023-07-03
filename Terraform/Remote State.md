# Remote State

- In Terraform, state locking refers to the mechanism that prevents concurrent access to the same Terraform state file by multiple users or processes.
- When multiple people or automation systems are working on the same infrastructure using Terraform, there is a possibility of conflicts if they simultaneously attempt to make changes to the state.
- State locking helps avoid these conflicts and ensures data consistency and integrity.
- Prevents Race Conditions: Without state locking, concurrent modifications to the state could lead to race conditions, where the last write might overwrite changes made by other users or processes.
- Data Integrity: State locking ensures that the Terraform state file is not corrupted due to simultaneous writes.
- Safe Collaboration: When multiple teams or individuals are working on the same infrastructure codebase, state locking allows them to collaborate safely without causing conflicts.
- Prevents Resource Corruption: Terraform relies on the state to manage the infrastructure, and a corrupted state file could lead to unintended resource destruction or misconfigurations.


## Example
- Let's consider a scenario where two DevOps engineers, Alice and Bob, are working on a shared Terraform codebase to manage the infrastructure of a web application. They both use the same state file stored in an S3 bucket as the backend.
- Alice and Bob each start a separate Terraform apply operation to update the infrastructure, intending to add different resources to support new features.
- Due to the absence of state locking, both apply operations start concurrently, and they both attempt to write changes to the shared state file simultaneously.
- A race condition occurs, and one of the apply operations completes first, overwriting the state file in the S3 bucket.
- When the second apply operation finishes, it writes its changes to the state file, overwriting the changes made by the first apply operation.
- As a result, the infrastructure ends up in an unexpected state with only one set of changes applied, and the other set of changes is lost.
- Had they used state locking, only one of them would have been allowed to apply changes at a time, avoiding the race condition and ensuring that both sets of changes were appropriately recorded in the state file.
- Some state storage backends like "Amazon S3" or "HashiCorp Consul" offer built-in locking mechanisms.


## Remote Backends
- Create an S3 Bucket: First, you need to create an S3 bucket in your AWS account to store the Terraform state file. You can do this manually through the AWS Management Console or use Terraform itself to provision the bucket.
- Configure Backend in Terraform Configuration: In your Terraform configuration files, add the following backend block to specify the S3 backend:

```
terraform {
  backend "s3" {
    bucket         = "your-s3-bucket-name"
    key            = "path/to/your/state.tfstate"
    region         = "your-aws-region"
    dynamodb_table = "your-dynamodb-table-name"  # Optional for state locking
  }
}

```
- Replace "your-s3-bucket-name" with the name of the S3 bucket you created, "path/to/your/state.tfstate" with the desired path and name for your state file, and "your-aws-region" with the appropriate AWS region code.
- The dynamodb_table attribute is optional but recommended for enabling state locking using DynamoDB as a lock table. You can create a DynamoDB table in the same AWS region and provide its name to enable locking.
- then do terraform init and apply
- By using the S3 remote backend, you can collaborate with other team members, share the same state file across environments, and safely manage infrastructure as code. It provides a centralized location for storing the Terraform state, making it easier to manage and maintain the infrastructure over time.

##  Terraform state commands
- ```terraform state show s3_bucket_finance```
- subcommands can be ```list, mv,pull, rm, show```
- 

















