

 - Configured to run in two or more AZ's, 1+ Nodes are placed into a subnet in each AZ and scales with load. 
 - DNS name of the load balancer points to all connected nodes. Each ELB has a A record DNS name.
 - If a node fails, it is replaced. If load increases to a node, others will be created to offset it. 
 - Internet Facing - nodes of the LB are given public and private IP Addresses
 - Inward/internal Facing - nodes of the LB are only given private IP addresses

 - Load Balancer nodes are configured with Listeners which accept traffic on a port & protocol and comminate with targets on a port and protocol, SUCH AS BACKEND INSTANCES, DOES NOT MATTER WHETHER THEY ARE PUBLIC OR PRIVATE. 
 - 8+ free IPs (/28) per subnet and /27 or larger subnet to allow for scaling the ELB.