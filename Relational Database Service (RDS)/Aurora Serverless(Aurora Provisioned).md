

## Personal Summary

 - It removes the need of overheading the DB's.
 - Scalable - ACU - Aurora Capacity Units
 - Aurora Serverless cluster has a MIN & MAX ACU
 - Cluster adjusts based on load
 - Can go to zero and be paused
 - Consumption billing per-second basis
 - Same resilience as as Aurora (6 copies across AZs)

 - ACU's are allocated from an AWS-managed pool of Capacity Units, they are stateless are used across many AWS customers.
 - When allocated to an Aurora serverless cluster, they have access to the cluster storage. 
 - Proxy fleet broker a connection between a client application and the Aurora serverless cluster. 
 - Because client isn't connecting to machinery providing the ACU, but an instance in the proxy fleet, connection and performance stays smooth.

 - Use Cases
	 - Infrequently used applications
	 - New applications
	 - Variable workloads
	 - Unpredictable workloads
	 - Developments and test databases
	 - Multi-tenant applications
	 -