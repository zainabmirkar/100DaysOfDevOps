# EBS SNAPSHOTS
- Ebs snapshots are point-in-time images/copies of your ebs volumes.
- Any data written to the volume after the snapshot process is initiated, will not be included in the resulting snapshot(but will be included in the future i.e. incremental update)
- snapshot is stored in s3 which you cannot access but you can access them using through ec2 api's. s3 bucket are not yours.
- per aws account 5000 ebs volumes can be created and 10000 ebs snapshots.
- ebs volumes are az specific however snapshots are region specific.
- any az in the region can use snapshot to create a volume.
- to migrate ab ebs volume from one az toanother, create a snapshot of the respective az and then create a ebs volume from that intended snapshot.
- if you are creating an ebs volume of a snapshot, its size can be equal to the snapshot or larger but never less.
