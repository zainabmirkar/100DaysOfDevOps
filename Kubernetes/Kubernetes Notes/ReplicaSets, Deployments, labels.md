### Labels

- Labels are key/value pairs that are attached to objects such as Pods. Labels are intended to be used to specify identifying attributes of objects
- by default label is run: podname
- k get pods --show-labels
- k label pod -l release=alpha1.1 work=tut
- k get pods -l run=new
- k get pods -l run!=new
- if you edit the pod spec file for label, new pod wont be created just the labels will get changed

###
cluster --> node --> namesapce --> deployment --> rs --> pods --> containers

### Namespaces
- In Kubernetes, namespaces provide a mechanism for isolating groups of resources within a single cluster.
- use lables inside namespace for segregating the resources

### deployments
- You can define Deployments to create new ReplicaSets


### replicasets
- A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time
- rc is no longer used
- k apply -f rs.yml
- k scale rs rs-demo --replicas=4
- what if we delete the rs
- When scaling down, the ReplicaSet controller chooses which pods to delete by sorting the available pods to prioritize scaling down pods based on the following general algorithm:
- Pending (and unschedulable) pods are scaled down first
- If controller.kubernetes.io/pod-deletion-cost annotation is set, then the pod with the lower value will come first.
Pods on nodes with more replicas come before pods on nodes with fewer replicas.
- If the pods' creation times differ, the pod that was created more recently comes before the older pod (the creation times are bucketed on an integer log scale when the LogarithmicScaleDown feature gate is enabled)

### annotations
- Annotations are key/value pairs.
- k annotate pod demopod maintainer='zain@gmail.com'

### deployments























