

## Personal Summary

 - IT IS BAD PRACTICE TO RUN A DB ON EC2 WITHOUT GOOD REASON
 - 1 instance running the db, app, and web server vs 2 instances (1 running the db and the other running the app and webserver)
 - Can have the two instances in the same AZ or split the two instances across two availability zones. 
 - Must be reliable and good communication between the two instances or the application will not function properly. 
 
 - WHY YOU SHOULDN"T
	 - access to the DB instance OS
	 - Advanced DB Option Tuning, as you gain access to the root user. 
	 - Vendor demands authentication not AWS
	 - Specific OS/DB Combination AWS doesn't provide
	 - Architecture AWS doesn't provide (replication and resilience)
	 - Decision makers who 'just want it'

	 - Admin Overhead - managing EC2 and DBHost
	 - Backup / DR Management
	 - EC2 is in a single AZ, if it goes down, access to the DB goes down. 
	 - Features - some of AWS DB products are amazing and are better to keep
	 - EC2 is ON or OFF - no serverless, no easy scaling available
	 - Replication - skills, setup time, monitoring & effectiveness
	 - Performance - AWS invest time into optimization and features, that this sole EC2 will not have access to.