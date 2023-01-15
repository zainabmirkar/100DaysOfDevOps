
# Storage in docker
https://www.waytoeasylearn.com/learn/storage-in-docker/

# Persistent Volumes
- A PersistentVolume (PV) is a piece of storage in the cluster that has been provisioned by an administrator.

# PVC
- A PersistentVolumeClaim (PVC) is a request for storage by a user. 
- It is similar to a Pod. Pods consume node resources and PVCs consume PV resources. Pods can request specific levels of resources (CPU and Memory).
- Claims can request specific size and access modes (e.g., they can be mounted ReadWriteOnce, ReadOnlyMany or ReadWriteMany, see AccessModes).


# Storage classes
- it is dynamic provisioning of volumes
- if the volume gets provisioned automatically when the application requires it, and that's where storage classes come in. With storage classes, you can define a provisioner, such as Google Storage, that can automatically provision storage on Google Cloud and attach that to pods when a claim is made. That's called dynamic provisioning of volumes.
- so we no longer need the PV definition, because the PV and any associated storage is going to be created automatically when the storage class is created.
- For the PVC to use the storage class we defined, we specify the storage class name in the PVC definition. 
- That's how the PVC knows which storage class to use.
- Next time a PVC is created, the storage class associated with it uses the defined provisioner to provision a new disk with the required size on GCP, and then creates a persistent volume, and then binds the PVC to that volume.
- ``` k get sc ``` to list the storageclasses



### Reference 
https://kubernetes.io/docs/concepts/storage/persistent-volumes/
