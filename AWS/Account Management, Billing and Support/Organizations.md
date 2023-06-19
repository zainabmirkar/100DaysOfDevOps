# Organizations

- allows to manage multiple aws accounts
- global service
- main account is the master account
- single payment method for all the aws accounts
- pricing benefits from aggregated usage
- volume discount for s3, ec2
- restrict account privileges using scp (Service Control Policies)
- pooling of reserved ec2 instances for optimal savings
- When using AWS Organizations, you can implement various multi-account strategies to effectively manage and govern your AWS resources.


- you can use multiaccount or one account multi vpc

# SCP
- retsrict account privileges
- scp does not have any effect on master account
- whitelist or blacklist iam actions
- applied at ou or account level
- looks just like iam policy
- applies to user, roles of the account, including root
- does not apply to service linked role
- does not allow anything by default




### multi account strategy in AWS.
- That means that you wanna create the accounts
- for example, per department per cost center, per environment, for example dev test and prod based on regular share restrictions.
- For example, if you don't want a service to be using an account you can use an STP or if you want to isolate the resources better you could have different VPC in different accounts and is also very good to have separate per account service limits and also isolated accounts for logging.
- So all of these could be multi account strategies is really up to each organization to choose what type of accounts they want.
- So the idea is that you have two options you can use Multi Accounts or One Account and Multiple VPC.

### Multi account vs one account multi vpc
- use tagging standars for billing purpose
- enable cloudtrail on all accounts, send logs to s3

## How to organize accounts?
- eg: sales ou we can have multiple sales account
- you can also have ou inside an ou. for example in production ou we can have a finance ou and so on
  
