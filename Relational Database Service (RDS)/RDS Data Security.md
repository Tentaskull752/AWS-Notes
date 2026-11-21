

## Personal Summary

 - Data between user and RDS (can be set to mandatory) can be encrypted by SSL/TLS/ 
 - RDS supports EBS volume encryption via KMS
 - Handled by HOST/EBS
 - AWS or Customer managed CMK generates data keys. These CMK keys are used to create Data Encryption Keys, these are given to the hosts, which then given to EBS to encrypt data.
 - Data keys used for encryption operations
 - Storage, Logs, Snapshots & replicas are encrypted.
 - Encryption cannot be removed.
 - RDS MSSQL and RDS Oracle support Total Data Encryption (TDE)
 - Encryption handled within DB engine
 - RDS Oracle supports integration with CloudHSM
 - Much stronger key controls (even from AWS)


 - With RDS Oracle - keys can be provided via CloudHSM - removing AWS from the chain of trust. 
 - ![[Pasted image 20251129115539.png]]


 - IAM Authentication for RDS
	 - Controlled by local Database Users, have their own username and passwords.
	 - This DB User is allowed to use AWS Authentication Tokens
	 - There are IAM Users and EC2 Roles present, and attached to these, are policies that attach that user or role to the DB User. 
	 - Now these two can perform AWS Authentication Token Creation, which can create a token with a 15-minute validity window to access the DB without using a password.
	 - ONLY FOR AUTHENICATION, NOT AUTHORIZATION.