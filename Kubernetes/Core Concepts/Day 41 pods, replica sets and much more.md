# PODS WITH YAML

- kubectl create -f pod.yaml
- kubectl get pods
- kubectl describe pod myapp-pod


# Replica sets 
- To prevent users from losing access to our application, we would like to have more than one instance or pod running at the same time.
- That way, if one fails we still have our application running on the other one.

# Replication Controller
- the Replication Controller ensures that the specified number of pods are running at all times even if it's just one or 100.
- the Replication Controller spans across multiple nodes in the cluster.
- It helps us balance the load across multiple pods on different nodes as well as scale our application when the demand increases.

### Difference between rc and rs
- Replication Controller is the older technology that is being replaced by Replica Set.
- Replica Set is the new recommended way to set up replication.


### Important point
- there were pods created before the creation of the Replica Set that match labels specified in the selector, the Replica Set will also take those pods into consideration when creating the replicas.

### Labels and Selectors
##### How does the Replica Set know what pods to monitor?
- There could be hundreds of other pods in the cluster running different applications. This is where labeling our pods during creation comes in handy. We could now provide these labels as a filter for Replica Set.
- Under the selector section, we use the match labels filter and provide the same label that we used while creating the pods. This way, the Replica Set knows which pods to monitor.

##### How do we update our Replica Set to scale to six replicas?
- Well, there are multiple ways to do it.
- The first is to update the number of replicas in the definition file to six. Then run the kubectl replace command to specify the same file using the -F parameter
and that will update the Replica Set to have six replicas.
- The second way to do it is to run the kube control scale command, use the replicas parameter to provide the new number of replicas and specify the same file as input. But it will not update replicas to 6 in the yaml file.

#### Commands
- to replace number of pods in the yaml file kubectl replace -f replicaset-app.yaml
- kubectl scale - -replicas=5 -f replicaset-app.yaml   Scale up
- kubectl scale - -replicas=1 -f replicaset-app.yaml  Scale down


# Deployments
- When we create a deployment, it creates a replica set, using the exact pod specification that we gave it.
- When we update a deployment and adjust the number of replicas, it passes that update down to the replica set.

### Reference 
https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/
https://semaphoreci.com/blog/kubernetes-deployment
