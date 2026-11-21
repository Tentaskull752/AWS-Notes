
- Makes cryptographic material (KEYS)
- Concern: KMS is a shared product, meaning other accounts within AWS utilize it.

- HSM is a true single-tenant Hardware Security Module provisioned by AWS and fully customer managed.. Can be run on-premises. 
- Fully FIPS 140-2 Level 3 (KMS is L2 Overall, some L3).
- Industry Standard APIs - PKCS#11, Java Cryptography Extensions (JCE), Microsoft CryptoNG (CNG) libraries
- Custom Key Store (KMS feature), can be used by CloudHSM to gain integration with AWS

- HSM are deployed in an AWS-managed CloudHSM VPC.
- Cluster is created within the CloudHSM VPC, and  there is HSM within each AZ within the cluster.
- HSMs keep keys and policies in sync when nodes are added or removed
- HSMs operated in an AWS managed HSM VPC, Interfaces are added to custom VPC. ANY SERVICE WITHIN THESE CUSTOM VPC, CAN USE HSM THROUGH THE INTERFACE.

- Client will need to be installed on the EC2 instance in order to access the HSM service. Once installed, can then utilized Industry standard APIs(PKCS#11, Java Cryptography Extensions, Microsoft NG Libraries)
- AWS provisions the HSM but have no access to secure area where key material is held

- No Native Integration between CloudHSM and AWS Products. e.g S3 SSE
- Offload the SSL/TLS Processing for Web Servers instead of having the EC2 instance doing it
- Enable Transparent Data Encryption (TDE) for Oracle Databases
- CloudHSM can protect keys for certificate authority (CA)