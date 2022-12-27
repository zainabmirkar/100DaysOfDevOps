# Namespaces

- kubectl get pods --namespace=dev <br/>
it will return all the pods in the dev namespace <br/>
 
- kubectl config set-context $(kubectl config current-context) --namespace=dev <br/>
to avoid mentioning namespace every time <br/>

- kubectl get pods --all-namespaces
to view pods in all namespaces












https://www.aquasec.com/cloud-native-academy/kubernetes-101/kubernetes-namespace/
