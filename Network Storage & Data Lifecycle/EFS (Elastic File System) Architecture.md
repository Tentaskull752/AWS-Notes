
## Personal Summary

 - A system that allows media that is accessible via EC2, to exist outside of the EC2. This keeps a single version of the media alive even as the EC2 is delete and replaced. Moves the EC2 towards statelessness. 
 - EFS is an implementation of NFS(Network File System)v4
 - EFS Filesystems can be mounted in Linux
 - Data in these files can be shared between many EC2 instances. 
 - Private service, via mounts targets inside a VPC
 - Can be accessed from outside the VPC on-premises - VPN or DX (Hybrid products)

 - Mount targets run from subnets within the VPC. They have IP addresses taken from the IP range of the VPC  they reside in. 
 - Need to have multiple mount targets (at least one) in each AZ within the VPC. 

 - EFS is for LINUX ONLY INSTANCES
- Two modes:
	- General Purpose - default, ideal for latency sensitivity use cases such as webservers, content management systems, home directories, or general file services.
	- Max I/O - scale to higher levels of throughput but trades off with higher latency. 
		- Burst - throughput scales with size of the file system. More data stored -> better performance
		- Provisioned - can specify throughput requirements despite the size of data within the file system.

	  - EFS File System Storage Classes
		  - Infrequent Access (IA): access data in a cost-effective way, but won't access it for long periods of time.
		  - Standard: data that is accessed and used for day-to-day.
	 - Lifecycle Policies can be used with classes. 