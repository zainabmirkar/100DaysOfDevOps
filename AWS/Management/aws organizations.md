## Hierarchy of service components

- organizations
- root : all the aws accountd and ou resideunder root. it is at the top
- ou : categorizing aws accounts. can connect below ou or below root
- accounts
- scp : permission boundary that sets the max permission level for the objects that is applied to

### account management
- centrally manage the aws accounts and their permissions with respect to iam, api etc

### consolidated billing
- centrally manage cost across accounts

### categorization and grouping of account


# SCP
- They provide a centralized way to control access to AWS services and resources.
- SCPs follow a "deny overrides allow" logic. If an SCP denies a particular permission, even if an IAM policy allows it, the denial takes precedence.
- SCPs provide flexibility in managing permissions. You can have different SCPs for different OUs, allowing you to tailor access controls to the specific needs of different parts of your organization.
- scp does not grant access, they add a guardrail to define what is allowed. you will still need to create policies to grant permissions


