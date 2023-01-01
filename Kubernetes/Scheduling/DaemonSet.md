# DaemonSet

- A DaemonSet ensures that all (or some) Nodes run a copy of a Pod. As nodes are added to the cluster, Pods are added to them. 
- As nodes are removed from the cluster, those Pods are garbage collected. 
- Deleting a DaemonSet will clean up the Pods it created.
- DaemonSets are like ReplicaSets, as in it helps you deploy multiple instances of pods.
- Say you would like to deploy a monitoring agent or log collector on each of your nodes in the cluster, so you can monitor your cluster better.
- A DaemonSet is perfect for that as it can deploy your monitoring agent in the form of a pod in all the nodes in your cluster. Then you don't have to worry
about adding or removing monitoring agents from these nodes
- When there are changes in your cluster as the DaemonSet will take care of that for you.

[Also Read](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/)
