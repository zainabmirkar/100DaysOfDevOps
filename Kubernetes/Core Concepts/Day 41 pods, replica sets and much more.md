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
