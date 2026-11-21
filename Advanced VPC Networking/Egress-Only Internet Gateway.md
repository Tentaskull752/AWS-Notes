
## Personal Summary

- Only allows connections to be from within the VPC to the outside
- IPv4 addresses are private or public
- NAT allows private IPs to access public networks
- ...without allowing externally initiated connections (IN)
- With IPv6 all IPs are public
- Internet Gateway (IPv6) allow all IPs IN and OUT.
- IPv6 WILL BE EXPOSED TO THE PUBLIC INTERNET 
- Egress-Only is outbound-only for IPv6
- Egress-Only Gateway is HA by default across ALL AZs in the region - scales as required
- Egress-Only has the exact same architecture as a normal Internet Gateway
- Default IPv6 Route ::/0 added to RT with eigw-id(egress-only gateway) as target
- Responses from software updates for example, are allowed back in as the initial response came from within the VPC