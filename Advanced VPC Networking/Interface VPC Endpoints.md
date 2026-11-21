
## Personal Summary

- Provide private access to public AWS Services
- anything NOT S3 and Dynamo DB historically, but NOW S3 IS SUPPORTED
- Added to specific subnets - an ENI - NOT HIGHLY AVAILABLE = AZ/SUBNET FAILS, SERVICE FAILS. One Endpoint to One Subnet, per AZ used in the VPC
- Network access can be controlled via SG's
- Endpoint Policies restrict what can be done with the endpoint
- TCP and IPv4 ONLY
- Uses PrivateLink - allows AWS or 3rd party services to be injected into VPC and gain Network Interfaces (useful when in highly regulated industry but want to give private access to a 3rd party service)

 - When you create a NEW endpoint in a particular region or for a particular service, you get a NEW DNS for the service endpoint
 - Endpoint Regional DNS
 - Endpoint Zonal DNS
 - Applications can use these optionally or...
 - ....PrivateDNS overrides the default DNS for services and creates a new DNS that points to your interface endpoint (NOW ENABLED BY DEFAULT). Services that don't use the PrivateDNS, it connects the normal way, by resolving an address, converting that to IP, Instance too NAT Gateway, to Internet Gateway, to the Service
 - "It's as if the service has been injected into the VPC"
 - "Private DNS associates a private R53 Hosted Zone to the VPC changing the default service DNS to resolve to the interface endpoint IP"