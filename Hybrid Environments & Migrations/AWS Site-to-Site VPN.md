
## Personal Summary

- Allows quickest link between AWS and something that is not AWS
- A logical connection between a VPC and on-premises network encrypted using IPSEC, running over the public internet 
- Full HA - if you design and implement it correctly 
- Quick to provision - less than an hour 
- VPN connects VPCs and private on-premises networks
- Virtual Private Gateway (VGW) - can be a target on one or more route tables/ create and associate with a single VPC
- Customer Gateway (CGW) - refers to logical configuration within AWS and the thing it represents (a physical device such as an on-premises server)
- VPN Connection between VGW and CGW

 - Border Gateway Protocol (Must be allowed by Customer Router or you CAN"T used Dynamic VPNS)

 - Static VPN
	 - Routes for remote side added to route tables as static routes
	 - Networks for remote side statically configured on the VPN connection
	 - NO load balancing and multi connection failover
- Dynamic VPN
	- Border Gateway Protocol is configured on both the customer and AWS side using ASN. Networks are exchanged viBGP
	- Multiple VPN connections provide HA and traffic distribution
	- Can communicate state of the links between VPG and Customer Gateway, allowing highly available architecture.
	- Route Propagation (if enabled) means routes are added to RT's automatically. Will learn routes for VPG whenever activated within a VPNs are active

 - VPN Considerations
	 - speed limitation - 1.25 Gbps
	 - Latency Considerations - inconsistent, public internet 
	 - Cost - AWS hourly cost, GB out cost, data cap (on premises)
	 - Speed of setup - hours... all SOFTWARE configuration/ BGP Support needed for Dynamic VPN
	 - Can be used as a backup for Direct Connect
	 - Can be used as a backup for a physical connection such as Direct Connect. "VPN's can be used as a backup; rather than using 2 connections for true HA, 1 can be Direct Connect and the VPN can be the second connection"
	 - Can be used with Direct Connect to setup that initial connectivity. Can use VPN initially for connection, then replace down the line with Direct Connect