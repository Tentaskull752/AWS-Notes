
### Personal Summary

Used to create private networks within AWS, that other private services will run from. Used to connect AWS private network to on-premise networks when creating a hybrid network. 

VPC is within AZ 1 and 1 region, it is private and isolated unless YOU decide otherwise

 - Two types of VPC: 
	 - Default VPC: ONE DEFAULT VPC PER REGION. Created by AWS, come pre-configured; lot less flexible than custom.
	 - Can have multiple Custom VPCs per region. Requires 100% through and through customization, also private by default.


VPC CIDR is a range of IP's that a VPC uses, anything trying to connect with that VPC has to go through the range of those IPs. 

VPC can be divided into subnets(subnetworks); each subnet located in a VPC is in ONE AZ. Preconfigured to have one subnet in each AZ.

The IP range of CIDR indicate the start and end range that those subnets will use.

CIDR range of Default VPC is 172.31.0.0/16 in every AZ.  The higher the /# is, the smaller the network is. /17 is half the size of /16, so two can fit in the /16. And 16 /20 subnets can fit into the /16 that the VPC uses.

/20 subnet in each AZ in the region.

Internet Gateway (IGW), Security Group (SG) & NACL can be security to prevent unwanted coming from the outside.

Subnets assign public IPv4 addresses.






### Revealing Questions







### Insightful Links