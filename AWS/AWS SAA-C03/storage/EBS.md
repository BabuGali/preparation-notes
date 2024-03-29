- Elastic Block Storage
- To attach EC2 instances
- EBS volume types fall into two categories
	- SSD ( Solid State Drive) - backend volumes
			- faster processing speed over HDD
			- low latency
			- shorter read/write time
			- costlier
			- more reliable
			- USB pen drives, SD cards, Micro SD cards
	- HDD ( Hard Disk Drive ) - backed volumes
		- can not be used as boot volume
		- high latency
		- longer read/write time
		- frequently accessed 
		- throughput-intensive workloads 
		- MapReduce, kafka, log processing
		- cheaper compare to SSD
		- In case of any error in the drive, the entire HDD may crash and result in loss of data. This makes it less reliable
-  Volume Types can be used as a boot volume
	- General Purpose SSD
	- Provisioned IOPS SSD
	- Instance Store
 ##### Instance Store
 - only at instance lunch time we can specify the instance store volume
 - you can't lunch instance store volume after instance launched it
- General Purpose SSD 
	- Transactional workloads
	- Low-latency interactive applications
	- Boot volumes
	- Development and test environments
- Provisioned IOPS SSD
	- Workloads that require:
		- Sub-millisecond latency
		- Sustained IOPS performance
###### Recycle Bin
- a data recovery feature that enables one to restore accidently deleted Amazon EBS snapshots and EMS-backed AMIs. If deleted, then can be retained if it is with in the retention period
##### Encryption
- Data in transit between an instance and an encrypted volume is also encrypted
- There is no direct way to change the encryption state of a volume
- All ESB types support the encryption
- all instance types not support encryption
- you can have encrypted and non-encrypted volumes on a single instance
##### Snapshot
- AWS does **not automatically back up data stored** on your Amazon EBS volumes
-  Snapshots are _incremental_ backups
- You can track the status of your EBS snapshots through CloudWatch Events.
- Charges for your snapshots are based on the amount of data stored
- Deleting a snapshot has no effect on the volume. Deleting a volume has no effect on the snapshots made from it.
- You can't delete a snapshot of the root device of an EBS volume used by a registered AMI. You must first deregister the AMI before you can delete the snapshot
- You can't delete a snapshot that is managed by the AWS Backup service using Amazon EC2.
- Although you can delete a snapshot that is still in progress, the snapshot must complete before the deletion takes effect.
- **Amazon Data Lifecycle Manager to automate** the creation, retention, and deletion of EBS snapshots and EBS-backed AMIs
-  Amazon Data Lifecycle Manager supports EBS-backed AMIs only, not instance store-backed AMIs.
- Snapshots of encrypted volumes are automatically encrypted.
- Volumes that you create from encrypted snapshots are automatically encrypted.
- When you copy an unencrypted snapshot that you own, you can encrypt it during the copy process.
- When you copy an encrypted snapshot that you own or have access to, you can reencrypt it with a different key during the copy process
- **Amazon EBS Snapshots Archive** is a new storage tier that you can use for low-cost, long-term storage of your rarely-accessed snapshots that do not need frequent or fast retrieval
- By default, when you create a snapshot, it is stored in the Amazon EBS **Snapshot Standard tier** (_standard tier_)
- Snapshots stored in the standard tier are incremental. This means that only the blocks on the volume that have changed after your most recent snapshot are saved.
- You can modify the permissions of a snapshot if you want to share it with other AWS accounts.
- Snapshots are constrained to the Region in which they were created. To share a snapshot with another Region, copy the snapshot to that Region and then share the copy