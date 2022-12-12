# GitHub Actions

- event - anyone creating a pull request, contributor joined, issue created etc.
- action - aasigning an issue to someone, putting a label etc.
- workflow - combination of actions make workflow.

## How GitHub Actions automate these workflows?
- Listen to an event.
- Trigger workflow
<br/>


![image](https://user-images.githubusercontent.com/85761276/207124564-5a58095e-dd48-44ba-86d4-e3ddc98c51ee.png)


## why github actions?
- use same tool instead of third party integration.
- setup is easy.
- tool for developers.
- You don't have to install anything, for example, if your environment requires node, node and docker will be configured for you rather than you installing everything.
- streaming, searchable and linkable logs.
- built in secret store.


## Events
- You can configure your workflows to run when specific activity on GitHub happens, at a scheduled time, or when an event outside of GitHub occurs.
- ![image](https://user-images.githubusercontent.com/85761276/207125954-0d79f97e-32d5-4665-a575-e24196cfc480.png) <br/>
you can run a workflow when a branch protection rule has been created or deleted.

## Workflows
- .github/workflows
- yaml syntax

[workflows](https://docs.github.com/en/actions/using-workflows/about-workflows)

[workflow syntax](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#about-yaml-syntax-for-workflows)

## actions
- resusable code
- action.yaml contains the metadata and index.js
- javascript actions, docker container actions and composite actions.


### Reference : 
https://www.youtube.com/watch?v=R8_veQiYBjI <br/>
https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions
