

## Personal Notes


  - Every subnet has an associated NACL, and it filters any data coming in and out of the subnet is affected. 
  - Connections between resources within a subnet, such as two EC2s are not affected. 
  - Inbound rules affect data coming in to the subnet
  - Outbound rules affect data going out to the subnet
  - Does not filter in terms of request or response, only direction. 
  - NACLs allow both explicit ALLOWS and explicit DENIES.
  - NACL's are STATELESS, both Request and Response parts of every communication need individual rules. 1x inbound and 1x outbound. 
  - Default NACL within a VPC: Inbound and Outbound Rules have the implicit deny all and an Allow ALL rule. All traffic is allowed, the NACL has no effect.
  - Custom NACLs: can be created for a specific VPC and are initially associated with NO subnets. They only have 1 inbound rule which is the implicit Deny all. All traffic is denied. ONLY 1 outbound rule, the implicit DENY.
  - IPs/CIDR, Ports & protocols - no logical resources recognized
  - NACLs cannot be assigned to AWS resources, ONLY SUBNETS
  - Use together with Security Groups to add explicit DENY (Bad IPs/Nets)
  - Each subnet only gets ONE NACL (Default or Custom)
  - A NACL can be associated with many subnets.