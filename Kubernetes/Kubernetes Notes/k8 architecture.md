
## Master node
- etcd
- kube-api-server
- kube-scheduler
- kube-controller-manager
- cloud controller manager


### Kube-api-server
- most important. if kube-api-server goes down the entire cluster goes down
- authentication
- authorization: RBAC sees if you have permission or not. if you can create a cluster or not. An RBAC Role or ClusterRole contains rules that represent a set of permissions. Permissions are purely additive (there are no "deny" rules).
- admission controllers: validating and mutating. Admission controllers limit requests to create, delete, modify objects. The admission control process proceeds in two phases. In the first phase, mutating admission controllers are run. In the second phase, validating admission controllers are run
- ``` cd /etc/kubernetes/manifests```
- ``` cat kube-apiserver.yaml | grep enable```
- watch for updates

### ETCD
- database. distributed key value store
- nosql database
- raft consensus: etcd is built on the Raft consensus algorithm to ensure data store consistency across all nodes in a cluster
- protobuf
- wal

### kube scheduler
-  assigns Pods to Nodes
-  schedule one Pod is split into two phases, the scheduling cycle and the binding cycle <br/>
  ![image](https://github.com/zainabmirkar/100DaysOfDevOps/assets/85761276/55012db3-7b7e-4127-99d2-0aca90c2df3f)

- https://kubernetes.io/docs/concepts/scheduling-eviction/scheduling-framework/

### kube controller manager
- In Kubernetes, a controller is a control loop that watches the shared state of the cluster through the apiserver and makes changes attempting to move the current state towards the desired state
- In Kubernetes, controllers are control loops that watch the state of your cluster, then make or request changes where needed. Each controller tries to move the current cluster state closer to the desired state.
- there are different types of controllers. Kubernetes comes with a set of built-in controllers that run inside the kube-controller-manager.


## Worked Node
- kube proxy
- kubelet
- cri
