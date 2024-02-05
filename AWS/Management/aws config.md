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
