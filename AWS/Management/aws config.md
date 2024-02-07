# AWS Config

- AWS Config provides a detailed view of the configuration of AWS resources in your AWS account.
- With AWS Config, you can review changes in configurations and relationships between AWS resources, explore resource configuration history, and use rules to determine compliance.
- existing managed rules cvers around 55 services
- we can also create custom config rules by using lambda functions
- aws cli, config rule development kit (RDK), opensource and requires latest cli. it is running lambda function in background

## Cloudformation Guard Rules
- can create rules
- based on clauses simpley tru or false statements
- validate cf change sets, json based conf files, k8 configurations
- use dsl and requires custom cli to be used
- recent version Guard 2.1

## Rule Configuration: Evaluation mode and trigger type
- evaluation mode means when the resource will be evaluated by the rule
- proactive mode: Use proactive evaluation to evaluate resources before they have been deployed. This allows you to evaluate whether a set of resource properties, if used to define an AWS resource, would be COMPLIANT or NON_COMPLIANT given the set of proactive rules that you have in your account in your Region.

- Detective mode: Use detective evaluation to evaluate resources that have already been deployed. This allows you to evaluate the configuration settings of your existing resources.

- some managed rules include parameters as well

### Insufficient data
- can be when the rule never evaluated the resoource
- when the resource has been deleted
- when a custom rule's lambda function is failing to send evaluation results to aws config

### Remediation
- 2 types manual and automatic(aws systems manager automation)
- if the resource is not remediated with automatic remediation, you can retry mechanism
- you can also use systems manager change manager to cinfigure the change as soon as possible or the next available window
- change apporvals can be configured

### Compliance packs
- Compliance Packs are collections of AWS Config rules and remediation actions that are bundled together to help you manage compliance at scale.
- Usage:
 - To use Compliance Packs, you can enable them through the AWS Management Console, AWS Command Line Interface (CLI), or AWS SDKs.
 - After enabling a Compliance Pack, AWS Config will automatically evaluate your resources against the rules included in the pack.








