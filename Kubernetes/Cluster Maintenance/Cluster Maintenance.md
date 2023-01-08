# Operating System Upgrade

- ``` kubectl drain node01```
  - You can purposefully drain the node of all the workloads. So that the workloads are moved to other nodes in the cluster.
  -  When you drain the node the PODs are gracefully terminated from the node that they’re on and recreated on another.
  - The node is also cordoned or marked as unschedulable. 
  - Meaning no PODs can be scheduled on this node until you specifically remove the restriction.

- Now that the PODs are safe on the other nodes, you can reboot the first node. When it comes back online it is still unschedulable
-  ```kubectl uncordon node1``` You need to uncordon it so that pods can be scheduled again.

- ```  kubectl cordon node1``` 
  - Cordon simply marks a node unschedulable.
  - Unlike drain it doesn’t terminate or move the PODs on an existing node. 
  - It simply makes sure that new PODs are not scheduled on that node.
    
## Backup and Restore
https://www.waytoeasylearn.com/learn/backup-and-restore/
