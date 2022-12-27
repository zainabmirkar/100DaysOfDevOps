# Service

- It is an object just like rs, deployments
- One of its use case is to listen to a port on the node and forward request on that port to a port on the Pod running the web application. This type of service is known as a NodePort service because the service listens to a port 
on the node and forward request to the Pods.
- The second is CluserIP, and in this case, the service creates a virtual IP inside the luster to enable communication between different services, such as a set of frontend servers
to a set of backend servers.
- The third is loadbalancer
