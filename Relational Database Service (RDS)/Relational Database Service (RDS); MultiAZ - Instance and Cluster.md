

## Personal Summary

 -Old Instance Architecture

 - There is the primary DB server (instance) that contains the DB's you're using.
 - A Standby DB instance in a second AZ exists, and synchronously contains the data within your primary DB. 
 - All accesses to the DB is done with the Database CNAME, that leads directly to the primary DB. 
 - Backups can occur by replicating the standby into S3 buckets that can then be moved across multiple AZ's. 
 - During the case of a failover, RDS swaps primary functioning to the standby DB instance, and the Database CNAME points to it as well. 
 - Not free tier, extra cost for replica
 - ONLY ONE STANDBY REPLICA, CAN'T BE USED FOR READS OR WRITES
 - 60-120 seconds failover
 - SAME REGION ONLY
 - AZ Outage, primary failure, manual failover, instance type change and software patching

-Multi AZ Cluster Architecture
 - RDS is capable of having one writer instance replicating to two reader instances (both in separate AZ's).
 - Write instance is like the Primary Instance that can perform reads and writes. 
 - Can only have two read replicas.
 - Data is "committed" when 1+ reader finishes writing
 - There is a reader endpoint that points to the primary reader and this allows that data to be replicated across the cluster for high availability and resiliency. 
 - Instance endpoints point at a specific instance. Only use these for testing, because these instances switch over to nothing in the case of an instance failure. 

  - 1 writer and 2 reader DB instances (different AZs)
  - Much faster hardware, Graviton + local NVME SSD Storage
  - Fast writes to local storage > flushed to EBS
  - Readers can be used for reads, allowing some read scaling. 
  - Replication is done using transaction logs...more efficient
  - Failover is faster - 35s + transaction log apply
  - Writes are "committed" when 1 reader has confirmed.