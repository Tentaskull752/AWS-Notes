

## Personal Summary

 - A managed database migration service
 - Runs a replication instance
 - Define Source and Destination Endpoints that point at Source and Target Databases.
 - One Endpoint MUST be on AWS. 
 - Replication Instance - an instance with migration software that can communicate with DMS.
 - Replication tasks are sent to these replication instances. 
 - A task moves data from the source database to the destination database, using the information in each respectively. 
 - Jobs can be:
	 - Full Load Migration - one off migration of all data from source to target DB.
	 - Full Load + CDC - migrates existing data and captures and sends any changes on the source after the initial migration to the target DB. 
	 - CDC - ONLY captures changes in the source data and sends to target DB after another engine like MYSQL sends the initial bulk of data. 

 - Schema (logical blueprint that describes organization and connections within a DB) Conversion Tool (SCT) can assist with Schema Conversion. 
- SCT is used when converting one database engine to another. When one engine isn't compatible in a certain environment
- ...including DB -> S3 (Migrations using DMS)
- SCT is not used when migrating between DB's of the same type
- ...On-premises MySQL -> RDS MySQL
- Works with OLTP DB Types (MYSQL, MSSQL, Oracle)
- And OLAP (Teradata, Oracle, Vertica, Greenplum)
  On-premises MSSQL -> RDS MySQL
- On-premises Oracle -> Aurora

 - Larger migrations might be multi-TB in size
 - ...moving data over networks takes time and consumes capacity
 - DMS can utilize snowball...
	 - Step 1:  Use SCT to extract data locally and move to snowball device
	 - Step 2: Ship the device back to AWS. They load it onto an S3 bucket
	 - Step 3: DMS migrates from S3 into the target store
	 - Step 4: Change Data Capture (CDC) can capture changes, and via 53 intermediary they are also written to the target DB. 

 - SCT IS ONLY MIGRATING DB WHEN THE ENGINE IS CHANGING