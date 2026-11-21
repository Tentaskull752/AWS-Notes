

## Personal Notes



 - VPC is a REGIONAL SERVICE - ALL AZs in the region
 - Isolated network
 - Nothing IN or OUT without explicit configuration. 
 - Flexible configuration - simple or multi-tier
 - Hybrid Networking - other cloud & on-premises
 - Default or Dedicated Tenancy: controls whether the resources created within the VPC are placed on. ON DEFAULT, you can switch later on, DEDICATED MEANS EVERYTHING IS DECICATED FOREVER AND THERES A COST
 - IPv4 Private CIDR Block is the main method of communication within a VPC. 1 Default Primary Private IPv4 CIDR Block when VPC is created. 
 - Min /28(16 IP) Max /16 (65,536) IP Addresses
 - Optional secondary IPv4 Blocks
 - Optional single assigned IPv6 /56 CIDR BLOCK. IP range is either assigned by AWS or you use your own addresses. 
 - Range of IPv6 are all public, but you still have to explicitly allow access.
 - VPC has full Route 53; VPC 'Base IP + 2' Address. 10.0.0.0.0 > 10.0.0.0.2
 - enableDNSHostnames - gives instances DNS names. 
 - enableDNSSupport - enables DNS resolution in VPC