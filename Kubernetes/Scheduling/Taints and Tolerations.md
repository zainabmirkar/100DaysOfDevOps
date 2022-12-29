### Taints
- They are used to set restrictions on what pods can be scheduled on a node.
- Instead of applying the label to a node, we apply a taint that tells a scheduler to repel Pods from this node if it does not match the taint.
-  Only those Pods that have a toleration for the taint can be let into the node with that taint.

### There are 3 taint effects
- NoSchedule - pods will not be scheduled on any node
- PreferNoSchedule - the system will try placing that pod on a node but it is not guaranteed
- NoExecute - pods won't be place on this node and existing pods will be evicted if they cannot tolerate that taint.
- kubectl taint nodes node01 app=blue:NoSchedule

### Tolerations
- they are added to pods

#### By default taint is applied to the master node that's why no pod is scheduled on master node.



### Also read
https://medium.com/kubernetes-tutorials/making-sense-of-taints-and-tolerations-in-kubernetes-446e75010f4e
