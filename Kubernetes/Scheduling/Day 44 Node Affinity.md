[First read Taints and Tolerations](https://github.com/zainabmirkar/100DaysOfDevOps/blob/main/Kubernetes/Scheduling/Taints%20and%20Tolerations.md)


# Node Selectors
- First label the nodes. kubectl label nodes node01 size=Large
- Then create a pod.yaml file. set nodeSelector size=large. When the pod is created it will be placed on node01 as desired.
- What if we have more complex requiremnts? It cannot be achieved by using node selectors.
- That's why we habe Node Affinity.

# Node Affinity
- Node affinity is conceptually similar to nodeSelector, allowing you to constrain which nodes your Pod can be scheduled on based on node labels.

### Types
- requiredDuringSchedulingIgnoredDuringExecution : The scheduler can't schedule the Pod unless the rule is met. This functions like nodeSelector, but with a more expressive syntax.
- preferredDuringSchedulingIgnoredDuringExecution : The scheduler tries to find a node that meets the rule. If a matching node is not available, the scheduler still schedules the Pod.
- requiredDuringSchedulingRequiredDuringExecution : It will evict any pods running on a node that do not meet the affinity rules.
- preferredDuringSchedulingRequiredDuringExecution

##### IgnoreDuring Execution means the pods will continue to run once they're scheduled even if nodeaffinity is changed.


## Taints and Tolerations vs Node Affinity
- a combination of taints and tolerations and node affinity rules can be used together to completely dedicate nodes for specific parts.


#### References
- https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#node-affinity
