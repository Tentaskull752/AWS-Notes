

 - ELB is a DNS A Record pointing at +1 Nodes per AZ
 - Nodes in (one subnet per AZ) can scale when needed as load increases
 - Internet-facing means nodes have public IPv4 IP addresses.
 - Internal is private only IPs
 - EC2 doesn't need to be public to work with a LB. 
 - Listener Configuration controls WHAT the LB does
 - 8+ free IPs per subnet, and /27 subnet to allow scaling 
 - Cross-AZ allows the load split between node's own EC2 instances to be spread evenly out amongst other node EC2. If one node has 4 instances, then each would get 12.5% of the load, then the other node with one instance would be giving 100% of that 50% load to that one instance. instead, the load is evenly broken against the 5 instances within both Az's together.