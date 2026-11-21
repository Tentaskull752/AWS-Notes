
- In-memory database for high performance, orders of magnitude faster than physical disc.
- Not permanent, used for temporary data
- Used to cache data - for READ HEAVY workloads with low latency requirements
- Reduces database workloads (cost efficient)
- Can store Session Data (Stateless Servers)

- Elasticache preserves Session States when one instance fails that a user is on. The user will be sent to the next instance, and their session will be retrieved from Elasticache
- This creates a Fault-tolerant system. And Aurora is receiving persistent data


- Memcached:
	- Simple data structures
	- No Replication
	- Multiple Nodes (Sharding)
	- No backups
	- Multi-threaded

- Redis:
	- Advanced structures
	- Multi-AZ
	- Replication (scale reads)
	- Backup & Restore
	- Transactions

- In-memory cache requires code changes to operate ************