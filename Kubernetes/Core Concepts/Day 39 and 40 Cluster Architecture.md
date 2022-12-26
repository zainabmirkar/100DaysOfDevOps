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
- kube-apiserver is the primary management component in Kubernetes. When you run a kubectl command, the kubectl utility is in fact reaching to the kube-apiserver.
- The kube-apiserver first authenticates the request and validates it.
- In this case, the API server creates a pod object without assigning it to a node. Updates the information in the etcd server,
- updates the user that the pod has been created.
- The scheduler continuously monitors the API server and realizes that there is a new pod with no node assigned.
- The scheduler identifies the right node to place the new pod on and communicates that back to the kube-apiserver.
- The API server then updates the information in the etcd cluster.
- The API server then passes that information to the kubelet in the appropriate worker node.
- The kubelet then creates the pod on the node and instructs the container runtime engine to deploy the application image.
- Once done, the kubelet updates the status back to the API server and the API server then updates the data back in the etcd cluster.
- It then retrieves the data from the etcd cluster and responds back with the requested information.

### Summary
- To summarize, the kube-apiserver is responsible for authenticating and validating requests, retrieving and updating data in the etcd data store.
- kube-apiserver is the only component that interacts directly with the etcd data store.
- The other components, such as the scheduler, kube-controller-manager and kubelet uses the API server to perform updates in the cluster in their respective areas.

### So how do you view the kube-apiserver options in an existing cluster?
- If you set it up with a kubeadmin tool, the kubeadmin deploys the kubeadmin-apiserver as a pod in the kube-system namespace on the master node.
- You can see the options within the pod definition file, located at etc/kubernetes/manifest folder.
- In a non-kubeadmin setup, you can inspect the options by viewing the kube-apiserver service located at etc/systemd/system/kube-apiserver.service.

# KUBE CONTROLLER MANAGER
- a controller is a process that continuously monitors the state of various components within the system and works towards bringing the whole system to the desired functioning state.

## Node controller
- The note controller tests the status of the notes every five seconds. That way the note controller can monitor the health of the notes. If it stops receiving heartbeat from a note the note is marked as unreachable but it waits for 40 seconds before marking it unreachable.
- After a note is marked unreachable it gives it five minutes to come back up. If it doesn't, it removes the PODs assigned to that note and provisions them on the healthy ones if the PODs are part of a replica set.

## Installing controller
- Download the Kube controller manager from the Kubernetes release page, extract it and run it as a service. When you run it, as you can see there are a list of options provided.
- This is where you provide additional options to customize your controller.
- Remember some of the default settings for node controller we discussed earlier such as the node monitor period, the grace period and the eviction timeout.
- There is an additional option called controllers that you can use to specify which controllers to enable.
- By default, all of them are enabled


## So how do you view the Kube controller managers server options?
- Again, it depends on how you set up your cluster. If you set it up with the Kube admin tool, Kube admin deploys the Kube controller manager as a POD in the Kube system namespace on the master node.
- You can see the options within the POD definition file located at Etc Kubernetes Manifest folder.
- In a non Kube admin setup, you can inspect the options by viewing the Kube Controller Managers service located at the services directory.

# KUBE SCHEDULER
- the scheduler is only responsible for deciding which pod goes on which node. It doesn't actually place the pod on the nodes.


# KUBELET
- The kubelet in the Kubernetes worker node registers the node with a Kubernetes cluster. When it receives instructions to load a container or a pod on the node,
- it requests the container runtime engine, which may be Docker, to pull the required image and run an instance.
- The kubelet in the Kubernetes worker node registers the node with a Kubernetes cluster.
- When it receives instructions to load a container or a pod on the node, it requests the container runtime engine, which may be Docker, to pull the required image
and run an instance.

# KUBE PROXY
- Kube-proxy is a process that runs on each node in the Kubernetes cluster. Its job is to look for new services, and every time a new service is created, it creates the appropriate rules on each node to forward traffic to those services to the backend pods.
- it is deployed as daemon set by kubeadm


# PODS
- Kubernetes does not deploy containers directly on the worker nodes.
- The containers are encapsulated into a Kubernetes object known as pods.
- A pod is a single instance of an application.
- A pod is the smallest object that you can create in Kubernetes.
- To scale up, you create new pods. And to scale down, you delete existing pod. You do not add additional containers to an existing pod to scale your application.

### can you have same containers in a single pod ?
- Sometimes you might have a scenario where you have a helper container that might be doing some kind of supporting task for our web application, such as processing a user and they're data processing a file uploaded by the user, et cetera, and you want these helper containers to live alongside your application container.
- In that case, you can have both of these containers part of the same pod.





#### Reference
https://k21academy.com/docker-kubernetes/kubernetes-architecture-components-overview-for-beginners/
