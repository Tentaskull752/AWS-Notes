

## Personal Notes


  - WATCH OUT FOR TRICK QUESTION SUGGESTINGS THAT ONE NAT GATEWAY IS TRULY REGIONLY RESILIENT. ONE IN EACH AZ IS NEEDED ALONG WITH A ROUTE TABLE.
  - If you ever need to use a NAT INSTANCE, the EC2(aka Nat Instance) automatically filters all traffic that it sends and receives. Traffic that is not the source or destination is instantly dropped. To get rid of this feature. Disable "Source/Destination Checks".
  -  If you value availability, bandwidth, low-level maintenance, and high=performance, YOU WANT A NAT GATEWAY. 
  - NAT Instances have more flexibility in customization compared to Nat Gateways; you cannot use it as a bastion host and it cannot do port forwarding because you cannot connect to it's OS. It is AWS-managed. 
  - NAT Instances are EC2s working as NATS, you can filter traffic using NACLs or SGs associated with that instance; NAT CANNOT UTILIZE SGS, ONLY NACLS.
  - NAT isn't required for IPv6. All IPv6 addresses in AWS are publicly routable.
  - The internet Gateway works with all IPv6 IPs directly. 
  - NAT GATEWAYS DO NOT WORK WITH IPv6!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
  - ::/0 Route + IGW will give Instance bi-directional connectivity. 
  - ::/0 Route + Egress-Only Internet Gateway - Outbound Only access to internet and AWS Public Service. 