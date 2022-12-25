# CLUSTER ARCHITECTURE

- The purpose of Kubernetes is to host your applications in the form of containers in an automated fashion so that you can easily deploy as many instances of your application
as required and easily enable communication between different services within your application. So, there are many things involved that work together.

- We have master and worker nodes.
- On the master, we have the etcd cluster, which stores information about the cluster.
- We have the kube scheduler that is responsible for scheduling applications or containers on nodes.
- We have different controllers that take care of different functions like the node controller, replication controller, et cetera.
- We have the Kube API server that is responsible for orchestrating all operations within the cluster.
- On the worker node, we have the kubelet that listens for instructions from the Kube API server and manages containers and the Kube Proxy that helps in enabling communication
between services within the cluster.

# ETCD
- distributed reliable key value store.
- install etcd by installing the binary then extract and run the etcd service.
- The advertised client URL. This is the address on which etcd listens. It happens to be on the IP of the server and on port 2379, which is the default port on which etcd listens.
- This is the URL that should be configured on the kube API server when it tries to reach the etcd server.
- default client that comes with etcd is the etcdctl where you can store and retrieve your key value pairs.
- ./etcdtl --version will give etcdctl version and api version.
- The etcd data store stores information regarding the cluster such as the notes, pods, convicts, secrets, accounts, roles, role bindings, and others.
- Every information you see when you run the kube control get command is from the etcd server.
- Every change you make to your cluster such as adding additional nodes, deploying pods or replica sets are updated in the etcd server.
- Only once it is updated in the etcd server is the change considered to be complete.
### Depending on how you set up your cluster, etcd is deployed differently.
- If you set up your cluster from scratch, then you deploy etcd by downloading the etcd binaries yourself, installing the binaries and configuring etcd as a service in your master node yourself.
- If you set up your cluster using kubeadm, then kubeadm deploys the etcd server for you as a pod in the kube system namespace.
- You can explore the etcd database using the etcd control utility within this pod.
- To list all keys stored by Kubernetes, run the etcd control get command.

### commands are different in version 3

- etcdctl snapshot save 
- etcdctl endpoint health
- etcdctl get
- etcdctl put

### To set the right version of API set the environment variable ETCDCTL_API command

- export ETCDCTL_API=3
- When API version is not set, it is assumed to be set to version 2. And version 3 commands listed above don't work. When API version is set to version 3, version 2 commands listed above don't work.

# KUBE-API SERVER




#### Reference
https://k21academy.com/docker-kubernetes/kubernetes-architecture-components-overview-for-beginners/
