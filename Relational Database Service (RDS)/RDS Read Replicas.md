

## Personal Summary

 - They are read replicas of the primary Read/Write instance. 
 - They are not part of the main DB instance, they have their own endpoint.
 - The Primary read/write has no knowledge of these read replicas. 
 - Asynchronous replication; data hits the primary instance (read/write), then the standby, then the read replicas. 
 - Synchronous means MULTI-AZ and Asynchronous means READ REPLICAS

 - 5x direct read-replicas per DB instance
 - Each providing an additional instance of read performance.
 - Read-replicas can have their own read-replicas; but lag becomes a problem. 
 - Global Performance Issues 

 - Snapshots & backups IMPROVE RPO
 - RTO's are a problem
 - RR's offer near zero RPO as the read replica is synced from the main DB instance.
 - RR's can be promoted quickly - low RTO; only use RR's to recover data during failure, not data corruption or it will obtain the same/similar failure. 
 - Read only - until promoted
 - Global availability improvements ... global resilience. 