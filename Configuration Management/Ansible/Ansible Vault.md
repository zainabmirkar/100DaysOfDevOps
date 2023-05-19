# Ansible Vault

- Ansible Vault is a feature in Ansible that allows you to encrypt sensitive data, such as passwords, API keys, and other secrets, within your playbooks or inventory files. 
- It provides a secure way to store and manage sensitive information in your Ansible projects.
- create encrypted playbook
```
ansible-vault create playbook.yml
```
- edit playbook
```
ansible-vault edit playbook.yml
```
- change password
```
ansible-vault rekey playbook.yaml
```

- to encrypt existing playbook
```
ansible-vault encrypt newplaybook.yml
```
