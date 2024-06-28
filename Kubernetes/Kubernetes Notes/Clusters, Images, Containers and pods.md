### Dockerfile
- not case sensitive

### Images
- never use latest tags fro images
- distroless images vs alpine
- distroless - made by google. very small in size, "Distroless" images contain only your application and its runtime dependencies. They do not contain package managers, shells or any other programs you would expect to find in a standard Linux distribution. best practice, more security

### Containers:

- stateless and stateful
- ephemeral containers: 

### Commands
- k get nodes -o wide
- k get events
- alais k=kubectl
- k describe node
- kubectl api-resources
- k apply -f pod.yml
- k delete pod/podname
- k exec -it -- bash (we dont exec in production env)
- k get pod/nginx -o yaml>1.yaml

### pods
- disposable and ephemeral

### ephemeral containers
- exec is not used in production
- Since Pods are intended to be disposable and replaceable, you cannot add a container to a Pod once it has been created. Instead, you usually delete and replace Pods in a controlled fashion using deployments.
- Ephemeral containers are useful for interactive troubleshooting
- not much used because you cant kill it
- ```kubectl debug <pod-name> --image=busybox --target=<container-name>``` In this command: <pod-name> is the name of the pod you want to debug.
- --image specifies the image to use for the ephemeral container.
- --target specifies the container you want to target within the pod.

### Static pods
- Static pods are a type of pod in Kubernetes that are managed directly by the kubelet on a specific node, rather than by the Kubernetes API server.
- Since the API server is not involved, static pods can be useful for running essential services on nodes that need to start up before the Kubernetes API server is fully operational.
- The configuration file that defines static pods is typically placed in a predefined directory (e.g., /etc/kubernetes/manifests). The kubelet scans this directory and creates or updates pods based on the contents of the files.
- Automatic Restart
- Use Cases: Static pods are often used for critical components that must be available during cluster startup, such as the kube-apiserver, kube-scheduler, and kube-controller-manager in a self-hosted Kubernetes setup.
- ![image](https://github.com/zainabmirkar/100DaysOfDevOps/assets/85761276/dc679d49-b57e-4068-9331-446266e5b3b4)
- kubelet directory
- ![image](https://github.com/zainabmirkar/100DaysOfDevOps/assets/85761276/27f46841-2c85-4b8f-8eaa-6072317318d4)

### daemon sets
- A DaemonSet ensures that all (or some) Nodes run a copy of a Pod.
- running a cluster storage daemon on every node
- running a logs collection daemon on every node
- running a node monitoring daemon on every node

### init containers
- runs first
- if the init container fails then the application container wont run
- runs in sequence ... if there are multiple init containers and if 1st one fails the others wont run
- work done then vanish

### side cars
- always there monitoring the application container
- restartpolicy: always
- Sidecar containers are the secondary containers that run along with the main application container within the same Pod. These containers are used to enhance or to extend the functionality of the primary app container by providing additional services, or functionality such as logging, monitoring, security, or data synchronization, without directly altering the primary application code.
- These can be started, stopped, or restarted without effecting the main application container and other init containers.

#### restart policy -> never, always, on failure


















