## Metrics Server

- You can have one Metrics Server per Kubernetes cluster.
- The Metrics Server retrieves metrics from each of the Kubernetes nodes and pods, aggregates them, and stores them in memory.
- The kubelet also contains a sub component known as the cAdvisor or Container Advisor.
- cAdvisor is responsible for retrieving performance metrics from pods and exposing them through the kubelet API to make the metrics available for the Metrics Server.


## Minikube
- If you're using minikube for your local cluster, run the command ```minikube addons enable metrics-server```

## Commands
- ```kubectl top node``` (This provides the CPU and memory consumption of each of the node)
- Use the ```kubectl top pod``` command to view performance metrics of pods in Kubernetes.


## Managing applications
- ```kubectl logs -f podname``` - to view containers logs
- Which containers logs would it show? If there are multiple containers within a pod, you must specify the name of the container explicitly in the command.
