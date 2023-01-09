
# Storage in docker
https://www.waytoeasylearn.com/learn/storage-in-docker/

# Persistent Volumes
- A PersistentVolume (PV) is a piece of storage in the cluster that has been provisioned by an administrator.

# PVC
- A PersistentVolumeClaim (PVC) is a request for storage by a user. 
- It is similar to a Pod. Pods consume node resources and PVCs consume PV resources. Pods can request specific levels of resources (CPU and Memory).
- Claims can request specific size and access modes (e.g., they can be mounted ReadWriteOnce, ReadOnlyMany or ReadWriteMany, see AccessModes).




### Reference 
https://kubernetes.io/docs/concepts/storage/persistent-volumes/
