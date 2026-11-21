

## Personal Summary

 - It is very different from RDS
 - Uses a "cluster"
 - Has a SINGLE PRIMARY INSTANCE +0 or more replicas
 - Has a cluster volume(ssd based), shared between all instances within the cluster; faster provision, and better availability and performance
 - Data is synchronously replicated (at storage level) between the replica instances within the cluster when data is written to the primary instance. 
 - Only the primary can write and read, while replicas can only read.
 - When there is a disc corruption/area, it uses other storage nodes to recover that down disc. 
 - Up to 15 replicas, any one of them can be the failover target.
 - All SSD Based - high IOPS, low latency. 
 - Storage is based on what's used
 - High water mark - billed for the most used.
 - Storage which is freed up can be re-used. Because storage is dedicated to the cluster, not the instances directly, the instances can be swapped out (removed and added).
 
 - Two endpoints: 
	 - Cluster endpoint - points to the primary instance
	 - Reader Endpoint - If replicas, it load balances to all replicas instances.

 - No free-tier option as Aurora does not support the micro-sized instances.
 - Beyond RDS singleAZ(micro) Aurora offers a better value.
 - Compute - hourly charge, per second, 10 minute minimum.
 - Storage - GB-month consumed, IO cost per request
 - 100% DB Size in backups included


 - Backups work in Aurora as they do in RDS
 - Restores create a new cluster
 - Backtrack can be used which allow in-place rewinds to a previous point in time
 - Fast Clones - create a new DB MUCH FASTER than copying all the data - copy-on-write. DOESNT MAKE A ONE TO ONE, references original storage and copies differences between the two only. Has to have a copy of the storage first.