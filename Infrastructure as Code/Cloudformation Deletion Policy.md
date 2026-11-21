
- Deletion of logical resources or stacks, results in the deletion of physical resources or stacks.
- Can result in data loss
- With Deletion Policy, you can customize the deletion process of a specific resource.
- ....Delete(default), Retain(physical resources are left untouched after stack deleted corresponding logical resources) or (if supported) Snapshot
	- Snapshot: EBS volume, Elasticache, Neptune, RDS, Redshift. The resource will be deleted, but not before a snapshot is created. And the snapshot will outlast the lifecycle of the stack. Clean up or charges will occur later on. DOES NOT SUPPORT EC2
- ONLY APPLIES TO DELETE....NOT REPLACEMENT/CHANGES