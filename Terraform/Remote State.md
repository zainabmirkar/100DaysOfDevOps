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
