
## Personal Summary


  - Placement groups allow manual placement for EC2s. 
- Three Types:
	- Cluster - packs instances close together.
		- create cluster group, and best practice is to launch all instances you plan on putting in the cluster at one time. 
		- launched into a single AZ, not specified. Locks cluster group to AZ that the first instance dropped in. 
		- All instances within the group use the same rack, and sometimes the same host. All members have direct connections to each other. (10GB per second instead of 5GB per second).
		- Lowest latency and highest packets per second possible in AWS. Need to be using instances with high-performing networking. 
		- If hardware fails, ALL instances will fail. 
		- once again, ONLY ONE AS 
		- can span VPC peers - but impacts performance
		- requires a supported instance type
		- USE SAME INSTNANCE TYPE, not mandatory
		- Uses: performance, fast speeds, low latency
	- Spread - keeps instances separated, where each instance is using different hardware. 
		- Maximum amount of availability and resilience for a group of instances.
		- each instance is in its own rack, has it's own networking and power supply. 
		- 7 instances per AZ - isolated infrastructure limit.
		- Provides infrastructure ISOLATION, each instance is ON ITS OWN
		- CANNOT use Dedicated instances or hosts
		- Uses: small number of critical instances that need to be kept separated from each other. 
		- IF ONE FAILS, THE OTHERS WILL CONTINUE FUNCTIONING 
	- Partition - groups of instances spread apart.
		- infrastructure where you have MAX 7 PARTITIONS.
		- Each partition within each AZ has it's own rack with it's own networking and power sourcing. 
		- CAN LAUNCH AS MANY INSTANCES AS YOU NEED INTO THE GROUP, CAN SELECT PARTITION MANUALLY OR HAVE EC2 DO IT.
		- GREAT FOR TOPOLOGY(types or data or applications loaded onto the instances, ex, 3 sets of data on three groups of partitions where there's 25 instances in each) AWARE APPLICATIONS. CAN ALSO HELP MINIMIZE FAILURE TO PART OF AN APPLICATION.