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


##### Reference
https://www.youtube.com/watch?v=6YZvp2GwT0A
