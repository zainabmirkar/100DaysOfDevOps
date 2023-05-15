# Playbooks

- written in yaml
- consists of variables, tasks, handlers, files, templates and roles
- composed of one or more modules
- consist of many sections like
  - target section: where the playbook tasks will be executed
  - variable section
  - task section


## handlers
- Handlers are special tasks that are executed only when notified by other tasks. They are typically used to perform actions that are dependent on the success or failure of other tasks.

- Handlers are defined within a playbook and are referenced by a unique name. When a task wants to notify a handler, it uses the notify directive, specifying the name of the handler.
- If multiple tasks notify the same handler, it will still be executed only once.

```
tasks:
    - name: Install package
      yum:
        name: your_package_name
        state: present
      notify: Restart Service
```
- In this example playbook, there are two tasks. The first task installs a package using the yum module and notifies the handler named "Restart Service." The second task configures a service by using a template and also notifies the same handler.
- The handlers section defines the "Restart Service" handler, which uses the service module to restart the specified service.
- When either of the tasks notifies the "Restart Service" handler, it will be executed once at the end of the playbook run.

## Variables
- In Ansible, variables are used to store and reference values that can be used across playbooks, tasks, and templates. 
 ```
 vars:
    http_port: 80
    database_name: mydb
 ```
 - In this example playbook, variables are defined at the play level using the vars keyword. Two variables, http_port and database_name, are assigned values 80 and mydb, respectively.


## Tasks
- Tasks can have various outcomes, such as reporting a change when a modification is made, indicating that no change occurred, or failing when an error occurs. These outcomes affect the behavior of the playbook and can trigger subsequent tasks or handlers.
- By defining tasks in your Ansible playbook, you can orchestrate a series of actions and configurations to manage and maintain the desired state of your infrastructure.
```
tasks:
    - name: Install package
      yum:
        name: your_package_name
        state: present
```
- The first task, "Install package," uses the yum module to install a package named "your_package_name" by specifying state: present. This task ensures that the package is present on the target hosts.





















