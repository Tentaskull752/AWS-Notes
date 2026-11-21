

## Personal Notes


  Network Address Translation: a set of processes - remapping SRC or DST IPs. 

 - IP Masquerading - hiding CIDR blocks behind one IP. Gives a whole range of Private CIDR range OUTGOING internet access. 
 - Public IPv4 addresses running out.
- NAT Gateway rests within the public subnet.
- It goes:
	- Private EC2 > Private Subnet Route Table > NAT Gateway >Internet Gateway > Internet
	- And when a response returns, the NAT Gateway changes the destination IP (NAT Gateway), to the private IP of the private subnet.
	- Private Subnet can have it's own Route Table, that sends traffic from resources within the private subnet to the NAT Gateway. 

 - "So the NAT Gateway takes all of the incoming packets from all of the instances its managing. And it records the information from the communication. It takes those packets, takes those sources of those packets and changes it to it's own IP address."
 - If you want to give an Instance it's own IPv4 address, only the Internet Gateway is needed.
 - If you want to give a private instance a public IPv4 address and internet and aws public service access, you need both NAT Gateway and Internet Gateway.
 - The Internet Gateway uses an ELASTIC IP; IPv4 addresses that are static and do not change. Allocated to your account in a region until un-allocated.
 - NAT Gateways are AZ resilient Service (HA in that AZ). 
 - For region resilience - NATGW in each AZ is needed. And Route Table for each AZ with that NATGW as the target.
 - AWS-managed, scales to 45 GBps, $ Duration & Data Volume. 
 - NATGW has two charges, an hourly base charge for use, and a data-processing charge per GB of data processed.