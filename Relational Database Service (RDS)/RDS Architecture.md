

## Personal Summary

 - Database as a Service (DBaas) - pay money and get a DB in return
 - But with RDS, you pay and get a database server (DBSaas) CAN HAVE MULTIPLE DATABASES on one DB Server (instance)
 - No hardware, OS, installation or maintaining of DB engine. No access to OS or SSH Access
 - Amazon Aurora is a different product

 - RDS Subnets are subnets that a RDS DB Instance can operate on. Can be placed in 1 or more AZ's. 
 - Picks one AZ for the primary and another for a standby instance.
 - RDS can be accessed from the vpc or any on premises resources.
 - RDS (BAD PRACTICE) can be accessed publicly from the internet via public addressing
 - RDS, each instance has it's own each dedicated EBS Storage 
 - Read Replicas can be placed within the RDS Subnet system; has asynchronous replication, meaning it can be within multiple AWS regions at once. Used for resilience and decreased read workload.

	- NOT BILLED ON USAGE, BUT RESOURCE AMOUNT. 
	- Costs:
		- Instance size & type
		- Multi AZ or not
		- storage & amount, per gig monthly fee
		- data transferred, charged by the gig
		- backups & snapshots
		- Licensing (if any private DB engine types used)