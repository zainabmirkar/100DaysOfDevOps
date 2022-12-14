# EBS SNAPSHOTS
- Ebs snapshots are point-in-time images/copies of your ebs volumes.
- Any data written to the volume after the snapshot process is initiated, will not be included in the resulting snapshot(but will be included in the future i.e. incremental update)
- snapshot is stored in s3 which you cannot access but you can access them using through ec2 api's. s3 bucket are not yours.
- per aws account 5000 ebs volumes can be created and 10000 ebs snapshots.
- ebs volumes are az specific however snapshots are region specific.
- any az in the region can use snapshot to create a volume.
- to migrate ab ebs volume from one az toanother, create a snapshot of the respective az and then create a ebs volume from that intended snapshot.
- if you are creating an ebs volume of a snapshot, its size can be equal to the snapshot or larger but never less.
- you can take a snapshot of a non root/non root volume even when its in the running state. This means you can still access it while snapshot is being processed. However the snapshot will only include the data that is written in the volume.
- The snapshot is created immediately but it may stay in the pending state until the full snapshot is created. This may take few hours for the first time. You can still access the non root volume, but the i/o will be slower because of ss activity.
- While in pedning state the snapshot will not include ongoing read and writes to the volume.
- To take complete snapshot of your ebs volume stop or unmount the volume.  
- To create a ss for root volume first stop the instance and then take ss.
- Deleting snapshot will only remove data exclusive to that snapshot.

# Incremental Snapshots
![image](https://user-images.githubusercontent.com/85761276/198816839-92de8ccd-2a9a-423b-b3d5-b874af1b9a5c.png) <br/>
<br/>
![image](https://user-images.githubusercontent.com/85761276/198816931-cfbed40b-68cb-420d-bf45-ecf3965bcc5f.png)



