
- It is a Petabyte-scale Database
- Can take data from S3, DynamoDB, Firehose, and DMS.
- Redshift Spectrum can perform direct queries on S3 without bringing data into the cluster.
- Direct query other Db's using Federated query. 
- Works off of OLAP (column based)
- Pay as you use
- Server-based
- One AZ/subnet in a VPC - network cost/performance
- There is a Leader Node and a Compute Node. The Leader Node coordinates complicated queries, taking in information from external standard-applications/workbenches or management applications or visualization. The compute nodes  run the queries: it's slide into partitions and they hold a portion of data from the og source (S3. for example). Helps resist complete failure
- Automatic backups for S3 for every 8 hours or every 5 GB. ONE DAY RETENTION PERIOD, configurable up to 35 days
- Manual backups must be managed by administrator

REDSHIFT DR and RESILIENCE

- Can put changed data within buckets that are in the same AZ/subnet that Redshift is in. These buckets can then be replicated into other AZs. IMPORTANT
- Copied snapshots can be sent to other regions for DR with a different configuration periods. 