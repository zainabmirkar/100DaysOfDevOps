# Configure Environment Variables in applications

- use env propertu which is an array
- this is a direct way of specifying env which is a key value format
- other ways are config maps and secrets


## Config Maps
- A ConfigMap is an API object used to store non-confidential data in key-value pairs. Pods can consume ConfigMaps as environment variables, command-line arguments, or as configuration files in a volume.

https://kubernetes.io/docs/concepts/configuration/configmap/

### Create configmaps 
#### Imperative approach
- ``` kubectl create configmap <configmap name> --from-literal=<key>=<value>``` and specify the required arguments

- ``` kubectl create configmap app-config --from-file=<path to file>```

#### Declarative approach
- create configmap.yaml file
- ``` kubectl apply -f configmap.yaml```
- view configmaps ```kubectl get configmaps```
- ``` kubectl describe configmaps```


### Configure configmaps in pod.yaml
- add a property to the container ```envFrom```
