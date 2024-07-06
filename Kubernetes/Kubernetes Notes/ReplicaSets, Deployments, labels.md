### Labels

- Labels are key/value pairs that are attached to objects such as Pods. Labels are intended to be used to specify identifying attributes of objects
- by default label is run: podname
- k get pods --show=labels

###
cluster --> node --> namesapce --> deployment --> rs --> pods --> containers

### Namespaces
- In Kubernetes, namespaces provide a mechanism for isolating groups of resources within a single cluster.
- use lables inside namespace for segregating the resources

### deployments
- You can define Deployments to create new ReplicaSets

### replicasets
- A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time
