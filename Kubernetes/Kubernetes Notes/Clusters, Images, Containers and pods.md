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
- 
