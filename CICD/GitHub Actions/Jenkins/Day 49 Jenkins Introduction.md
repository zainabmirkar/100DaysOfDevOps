# Jenkins
### One example of how Jenkins can be used is as follows:
- A developer commits code changes to a version control system (such as Git)
- Jenkins detects the changes and automatically pulls the latest code from the version control system
- Jenkins then runs a series of tests (such as unit tests and integration tests) to ensure that the code changes did not break any existing functionality
- If the tests pass, Jenkins can then automatically deploy the code changes to a staging or production environment
- By automating this process, Jenkins can help to reduce errors and improve the efficiency of the software development process.


- Master server: controls the pipelines and schedules builds to agents
- Agents/Minions: run the build in the workspace

#### There are 2 types of agents
- ```Permanent agents:``` these are basic linux/windows servers. you need to have java installed.
- ```Cloud agents:``` Docker, K8 and aws fleet manager

### Build Types
- ```Freestyle Build:``` Basically they are shell scripts running on a server that can be triggered by specific events. They're very easy to use.
- ```Pipelines:``` A Pipeline’s code defines your entire build process, which typically includes stages for building an application, testing it and then delivering it. They user jenkinsfile written in groovy syntax.

### Poll SCM
- In Jenkins, "Poll SCM" is a feature that allows the Jenkins server to periodically check the source code management (SCM) system (such as Git or SVN) for changes.
- If changes are detected, Jenkins will automatically trigger a new build.
- The "Poll SCM" feature can be configured in the Jenkins job settings. You can specify the schedule (e.g. every 15 minutes) and the SCM to poll (e.g. Git). Jenkins will then check the SCM at the specified intervals, and if changes are detected, it will trigger a new build.
- It's also important to mention that "Poll SCM" is not the only way to trigger builds on Jenkins, other options include webhooks and manual triggers, but it's a simple and effective way to setup a basic CI pipeline.


##### Reference
https://www.youtube.com/watch?v=6YZvp2GwT0A
