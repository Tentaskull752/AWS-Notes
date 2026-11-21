

## Personal Summary

 - Allows global database replication from a primary region to up to 5 secondary regions. 
 - Replication occurs from the storage layer; one second replication time (RTO and RPO) from the primary to the secondary regional databases

 - Uses:
	 - Cross-region Disaster Recovery and Business Continuity. 
	 - Global Read Scaling - low latency performance improvements
	 - Replication has no impact on DB performance as it occurs on the storage layer, not directly against the instance.
	 - Secondary regions can have 16 read replicas, any one of these can be promoted to read/write in the case of a disaster event. 
	 - 5 MAX SECONDARY REGIONS