
## Personal Summary

- Provides managed-file transfer service; supports transferring TO or FROM S3 and EFS
- Provides managed "servers" which supports protocols
- File Transfer Protocol (FTP) - Unencrypted file transfer
- File Transfer Protocol Secure (FTPS) - File Transfer with TLS encryption a little more secure
- Secure Shell (SSH) File Transfer Protocol (SFTP) - File transfer over SSH
- Applicability Statement 2  (AS2) - Structured B2B Data
- Identities - Service Managed, Directory Service, Custom (Lambda/APIGW)
- Managed File Transfer Workflows (MFTW) - serverless files workflow engine

- So if you need to interact with S3 or EFS where you have existing workflows and can't change applications, you can used AWS Transfer Family

- Servers are the front-end access points to your storage. Support back-end storage such as S3. How to access depends on access endpoint configuration
- Multi-AZ - Resilient and Scalable
- Provisioned Server per hour $ + data transferred $
- FTP and FTPS - Directory Service or Custom IDP only
- FTP -  VPC only (cannot be public)
- AS2 VPC Internet/Internal ONLY
- If you need to access S3/EFS, but with  existing protocols
- ...integrating with existing workflows
- ...or using MFTW to create new ones

Public Endpoint:
- Accessible via public internet
- Only has SFTP endpoint
- Has a Dynamic IP (can  change), managed by AWS SO USE DNS
- can't control who accesses it via security groups or network control groups

VPC - Internet:
 - Uses both SFTP and FTPS
 - Can be connected from connected business networks: anything using a VPN or direct connect, ANYTHING  WITH A CONNECTION INTO THE VPC
 - Static IP that can be controlled with security groups and network control groups.
 - Allocated an Elastic IP and allows access over public internet and within VPC from corporate network

VPC - Internal:
 - Can use the endpoints of VPC Internet + AS2
 - 