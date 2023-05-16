# Adhoc Commands

- In Ansible, ad hoc commands refer to the commands that can be executed directly from the command-line interface without the need for writing and maintaining a playbook. 
- adhoc means temporary
- can do small tasks
- not used for configuration management and deployment
- no idempotency. executes same command again even if it has been completed

## Commands
![image](https://github.com/zainabmirkar/100DaysOfDevOps/assets/85761276/8beca1d8-33c5-4c86-a3a2-bcf151972d99)

- -all for all groups, else you specify group name eg: production 


![image](https://github.com/zainabmirkar/100DaysOfDevOps/assets/85761276/686dca95-a5dd-4318-ad0a-3ce22f2f3c59) <br/>
- create a file on all servers




# Modules
-  modules are pre-built scripts or programs that can be executed on remote systems to perform specific tasks.
- library of modules can reside in any location. there are no databases
- state= absent state=present state= latest is used
- latest is for updating
- use -b for sudo privileges
- Idempotency is present. work completed will not happen again

```
ansible production -m setup
```
## modules examples
- copy module
- gather facts module
- service module
- file module
- command module
- package module
- user module
- get_url module

## Difference between modules and adhoc-commands
- -m is in modules
- -a is present in both stands for argument






