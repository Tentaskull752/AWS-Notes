

## Personal Notes


 - Subnets inside VPCs are entirely private as default. 
 - AZ Resilient
 - Subnet is a subnetwork of a VPC - within a particular AZ. AZ fails, the subnet and any services within it fail. 
- 1 subnet is created within a specific AZ in a region, never more. 
- But one AZ can have many subnets.
- IPv4 CIDR is a subset of the VPC CIDR
- Cannot overlap with other subnets
- Optional IPv6 CIDR (/64 of the /56 VPC - space for 256)
- There is free communication between subnets within a single VPC. 
- 5 ADDRESSES IN EACH VPC SUBNET NOT TO USE: 
	- Network Address (10.16.16.0)
	- Network+1 (10.16.16.1) - VPC Router
	- Network+2 (10.16.16.2) - Reserved (DNS*)
	- Network+3 (10.16.16.3) - For future use
	- Broadcast Address 10.16.31.255 (Last IP in subnet)

 - VPC has a configuration object applied to it called DHCP Options Set (Dynamic Host Config. Protocol); how computers receive IP addresses automatically. One DHCP applied to one VPC at one time. Can control DNS servers, TP servers. You can create option sets but cannot edit them. 
 - Auto Assign Public IPv4: an options that can automatically give a Public IPv4 address and make a subnet public.
 - Auto Assign Public IPv6: an option that can automatically give a Public IPv6 address to resources within subnet/VPC