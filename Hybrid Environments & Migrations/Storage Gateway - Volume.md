
## Personal Summary

- Runs as a virtual machine (or hardware appliance) on premises
- Acts as a bridge between storage on premises and AWS
- Presents storage  using iSCSI, NFS, or SMB
- Integrates with EBS, S3 and Glacier within AWS
- Migrations, Extensions, Storage tiering, DR and Replacement  of backup systems

Stored Mode:
- Storage Gateway has local  storage and it is the primary storage of the volumes presented to servers.
- Migrations, Extensions, Storage tiering, DR and Replacement  of backup systems
- Upload Buffer: any data written to the primary storage is written here temporarily. 
- Data is copied into S3 via EBS Snapshot CONSTANTLY
- Great for full disk back ups
- DOES NOT IMPROVE DATACENTER  CAPACITY, MAIN COPY OF DATA IS STORED ON THE GATEWAY
- Can have 32 volumes for gateway and 16 TB for each volume (512 TB)

Cached Mode:
- Primary location of data is no longer on the physical premises, but in AWS' S3. 
- Stored in an AWS-managed section of S3, can't just open the bucket and view the data (also can't because it's raw data, not objects or images)
- ONLY THE FREQUENTLY ACCESSED DATA IS STORED LOCALLY
- ALLOWS IMPROVING OF DATACENTER AS ON-PREMISES CAN INCLUDE STORAGE WITHIN AWS AS PRIMARY LOCATION
- A single gateway can handle 32 TB per volume, and 32 volumes MAX for 2 PB of data