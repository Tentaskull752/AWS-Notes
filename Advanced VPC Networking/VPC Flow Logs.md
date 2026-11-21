
## Personal Summary

- ONLY CAPTURE PACKET METADATA (Source/Destination IP and ports and packet size) (NOT CONTENTS). Anything concerning the flow of data through the VPC
- Monitors can be attached to a VPC - ALL ENI's in that VPC
- ...Subnet - All ENI's in that Subnet
- ENIs directly
- FLOW LOGS ARE NOT REALTIME 
- Log Destination: S3 or CloudWatch Logs
- Can access it progmatically or through the CloudWatch console
- ...or Athena for querying (only billed for data as it's ran through the product and stored in S3)

 - Flow logs capture metadata from the capture point downwards (VPC -> Subnet(s) -> Interface(s))
 - ICMP = 1, TCP = 6, UDP = 17
 - IF YOU SEE AN ACCEPT AND A REJECT FOR THE SAME SOURCE AND DESTINATION OF TRAFFIC, YOU HAVE A SG AND A NETWORK ACL RESTRICTING TRAFFIC FLOW
 - SG's are state, they see the flow between both parties as 1 interaction
 - ACL see's 2 transactions, the request and the response; it can allow the first, while denying  the second
 - To and from 169.254.169.254, 169.254.169.123, DHCP, Amazon DNS server & Amazon Windows license not recorded