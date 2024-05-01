
#### Master node
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
- 
