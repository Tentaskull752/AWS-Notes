

## Personal Summary

 - Fills gap between RDS and EC2 Instance running a DB Engine.
 - RDS is fully managed - OS/Engine access is limited.
 - DB on EC2 is self managed - but has overhead.
 - Currently works for MS SQL and Oracle
 - Can connect using SSH, RDP, Session Manager
 - RDS Custom is operating within your AWS Account, unlike RDS. RDS injects Elastic Network Interfaces into your VPC, that's you access RDS, but it's different for RDS Custom.
- RDS Custom Database Automation Settings must be paused before performing changes to RDS Customization, then turned on again afterwards. 
- ![[Pasted image 20251129121104.png]]