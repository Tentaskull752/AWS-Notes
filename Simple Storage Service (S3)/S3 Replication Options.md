
## Personal Notes

  Cross-Region Replication(CRR): Allows replication of source bucket to other buckets in different AWS regions.
  Same-Region Replication(SRR): Allows replication of source bucket to other buckets in the same AWS region.

- An IAM Role is created for S3 to assume it; giving S3 permission to read objects in the bucket and to replicate and encrypt those objects to a destination bucket. 
- In CRR, the source bucket utilizing IAM role isn't trusted by the destination bucket by default. A bucket/resource policy will need to be created within the destination bucket to allow IAM roles to audit and replicate objects into it.
- All objects or a subset(group of objects selected by an applied filter) are replicated into a destination bucket. 
- A storage class is selected for the objects. The same storage class (standard initially) MUST be used by both the source and dest. bucket.
- Ownership belongs the account that owns the source bucket; the replicated product does not belong to the dest. bucket, meaning it can't read the objects within itself. There is an option to override this so the dest. bucket owns this replicated product.
- Replication Time Control (RTC): adds a guaranteed 15-minute SLA to replication requests for objects. This is for ex. strict deadlines are requiring near-perfect syncing between the two buckets at all times. 
- BY DEFAULT, REPLICATION IS NOT RETROACTIVE & VERSIONING NEEDS TO BE ON. YOU ENABLE REPLICATION ON THE TWO BUCKETS, AND OBJECTS AFTER THIS ARE CAPABLE OF REPLICATION, NOT OBJECTS BEFORE THIS SWITCH ON. 
- Batch replication can be used to replicate existing objects.
- One-way replication source to Destination (or bi-directional)
- Replication can handled unencrypted, SSE-S3 & SSE-KMS (with extra config), SSE-C
- Source bucket owner needs permissions to objects.
- Will not replicate system events (ONLY USER EVENTS), can't replicate any objects using Glacier or Glacier Deep Archive.
- NO DELETES (Delete Markers) are not replicated by default.
- USES
- SRR - Log aggregation
- SRR - PROD and TEST Sync
- SRR - Resilience with strict sovereignty
- CRR - Global Resilience Improvements
- CRR - Latency Reduction