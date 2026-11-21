
## Personal Summary


- Roles that an Instance can assume, and anything within it are granted the same permissions.
- Instance Profile is a wrapper around an IAM Role, it is attached to the EC2 instance, and it allows permissions to get inside the instance. When you create an Instance Role, a profile is created simultaneously and same name. If you use command line or cloud formation, you must create both. 
- Temporary Credentials are delivered to EC2 Service via instance meta-data. An application within the instance can use these credentials to utilize the permissions. These credentials are always valid and renewed before they expire as long as the application within the instance keeps checking the meta data for the values. 
- iam/security-credentials/role-name
- SHOULD ALWAYS USE ROLES WITH TEMP. CREDNETIALS INSTEAD OF STORING ACCESS KEYS LONG TERM. 
- Command lines within the EC2 that's attached to the Instance Role can use those permissions as well.