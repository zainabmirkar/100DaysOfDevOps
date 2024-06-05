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
