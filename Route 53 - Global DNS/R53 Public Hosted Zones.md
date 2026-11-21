
## Personal Summary

- A R53 Hosted Zone is a DNS DB for a domain ex. animals4life.org
- Globally resilient (multiple DNS Servers)
- Created with domain registration via 53, can ALSO be created separately
- Host DNS Records (A, AAAA, MX, NS, TXT)
- Hosted zones are what the DNS system references, AUTHORITATIVE for a domain

 - Public Hosted Zone:
	 - DNS database (zone file) hosted by R53 (public name servers)
	 - Accessible from the public internet & VPCs
	 - Hosted on "4" R53 Name servers specific for the zone
	 - use "NS records" to point at these Name Servers (connect to global)
	 - Resource Records (RR) created within the Hosted Zone
	 - Externally registered domains that point at R53 Public Zone
	 - PHZ can also be accessed through VPC side via internal IP address
	 - VPC +2 is the DNS resolver, allowing querying of R53 public and internet hosted DNS zones