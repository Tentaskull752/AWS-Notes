
## Personal Summary

- Provides a managed directory, stores users, objects(users, groups, computers, servers, file shares), and other configuration.
- Holds all of these objects with a structure. Branches out out from a single point. 
- Multiple trees can be grouped into a forest
- Commonly used in Windows Environments
- Sign-in to multiple devices with the same username/password provides centralized managements for assets
- Commonly used with Microsoft Active Directory Domain Service (AD AS)
- ....alternative to AD AS is SAMBA, but only provides partial compatibility with active directory.

- Directory Service
	- AWS Managed implementation, no ADMIN OVERHEAD
	- Runs within a VPC, it's a Private Service
	- To  implement HA...by  deploying into multiple subnets/AZ's
	- Some AWS services NEED a directory  e.g.  Amazon Workspaces (NEEDS to be a directory managed by AWS)
	- To join EC2 instances to a domain via AWS tools, you NEED a directory managed by AWS
	- Can be isolated with no other directories....
	- or integrated with  existing on-premises system
	- Or acts as a 'proxy' back to on-premises

-  Simple AD, is an open source directory of SAMBDA meant to cooperate with Directory Service as much as possible. 
- Up to 500 users (small) or 5,000 users (large)
- Designed to be used in isolation, not with on-premises devices
- Can be accessed directly, or through Directory Service connected with the Simple AD
- A Trust Relationship can be created between AD Mode and on-premises directory through a VPN.
- Resilient if the VPN Fails...services in AWS will still be able to access the local directory running in Directory Service

- AD Connector: Allows AWS services which NEED a directory to use an existing on-premises directory. Primary Directory is located on-premises requests from AWS are proxied back to the existing directory
- If private connectivity fails...the AD proxy wont function - interrupting service at the AWS Side
- DONT NEED TO PROVISION AN ADDITION DIRECTORY SERVICE TO USE AWS SERVICES. Use only when already have on-premises directory and just want to use AWS Products and Services that need a directory, without deploying a brand new one

- Simple AD - The Default. Simple requirements. A directory in AWS
- Microsoft AD - Applications in AWS which  need MS AD DS, or need to Trust AD DS
- AD Connector - Use AWS Services which need a directory without storing any directory info in the cloud ... proxy to your on-premises Directory. Have to point it back to on-premises (fully functiong) environment