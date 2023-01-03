# Rolling Updates and Rollbacks

- you can see the status of your rollout
``` kubectl rollout status deployment/myapp-deployment ```

- see the revisions and history of the rollout
``` kubectl rollout history deployment/myapp-deployment```

## rolling update
- We take down the older versions and bring up the newer versions one by one. 
- This way the application never goes down.
- It is the default deployment strategy.

## Rollback
- Say, for instance, once you upgrade your application, you realize something isn't very right.
- Something's wrong with the new version of build you used to upgrade, so you would like to roll back your update.
- Kubernetes Deployments allow you to roll back to a previous revision.
- To undo a change, run the Cube Control Rollout Undo command followed by the name of the deployment.
- The deployment will then destroy the pods in the new ReplicaSet and bring the older ones up in the old ReplicaSet, and your application is back to its older format.

``` kubectl rollout undo deployment/myapp-deployment ```

## Imp
- When you compare the output of ```kubectl get replicasets``` 
- Before the rollback, the first ReplicaSet had zero pods and new ReplicaSet had five pods, and this is reversed after the rollback is finished.
