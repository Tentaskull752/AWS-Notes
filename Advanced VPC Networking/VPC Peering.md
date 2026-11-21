
## Personal Summary

- Allows creation of private network connection between two VPC (NO MORE THAN TWO)
- Can be same region or cross region and same/cross-account
- (optional) Public Hostnames resolve to private IPs
- Same region SG's can reference peer SGs (Other regions will need to reference IPs or IP Ranges)
- VPC Peering DOES NOT support transitive peering. If VPC A is connected to VPC B, which is connected to VPC; VPC A IS NOT CONNECTED TO VPC C!!!

 - Route tables at both sides of the peering connection are needed, directing traffic flow for the remote CIDR/IP of the other VPC at the PEER GATEWAY OBJECT. 
 - IP RANGES CANNOT OVERLAP WHEN USING VPC PEERING; NEVER USE THE SAME ADDRESS RANGES IN MULTIPLE VPCS
 - When using Cross-region peering connections, communication is encrypted and transits over the AWS global network.