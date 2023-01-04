# Configure Environment Variables in applications

- use env property which is an array
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


## Secrets
- for storing sensitive information.

#### imperative approach
- ```kubectl create secret generic <secret-name> --from-literal=<key>=<value>```

#### Declarative Approach
- In this approach we create a definition file just like how we did for the ConfigMap. The file has apiVersion, kind, metadata and data.
- we have specified the data in plain text which is not very safe. 
- So while creating a secret with declarative approach you must specify the secret values in a hashed format.
- But how do you convert the data from plain text to an encoded format? On a Linux host run the command echo -n followed by the text you are trying to convert, which is mysql in this case and pipe that to the base64 utility.
- ``` echo -n mysql | base64```
- ``` kubectl get secrets```
- ```kubectl describe secrets```
- ``` kubectl get secret app-secret -o yaml``` output will be in yaml file





