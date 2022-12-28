# Service

- It is an object just like rs, deployments.
- It provides stable ip which doesn't change. kubectl get pod -o wide to see ip
- provides loadbalancing.
- One of its use case is to listen to a port on the node and forward request on that port to a port on the Pod running the web application. This type of service is known as a NodePort service because the service listens to a port on the node and forward request to the Pods.
- The second is CluserIP, and in this case, the service creates a virtual IP inside the luster to enable communication between different services, such as a set of frontend servers.
to a set of backend servers.
- The third is loadbalancer

### Important points
- target port where the service forwards the request to
- second port is on the service itself
- the service has its own ip which is known as cluster ip
- we have port on the node itself which we use to access the web servier externally that is known as the node port. range is between 30000 to 32767. if you don't provide a nodeport in the service.yaml file then a free port is automatically assigned between the range.
- pod was created with a label. mention the selector in the service.yaml
- kubectl create -f service.yaml (to create the service)
- kubectl get services(to list the services)

### Note
- The service is created in the exact way whether there are multiple pods in the same node or pods across multiple node. When the pds are removed or added the service updates itself making it very adaptive and flexible.

# Cluster IP
- There are multiple pods running for frontend, backend. These pods wants to interact with each other. As we know the ip of the pods is static meaning it can change everytime a pod is created. So K8 service can group the pods together and provide a single interface to access the pods. he request is then forwarder to any pod randomly.


# Loadbalancer
- the users wants a single url to access the application
- just set the type to loadbalancer. this works only with supported cloud platforms







#### Also read 
https://www.bmc.com/blogs/kubernetes-services/
