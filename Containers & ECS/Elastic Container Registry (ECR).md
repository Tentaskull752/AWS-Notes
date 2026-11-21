
#### Personal Summary 

 - Managed Container image registry service within/for AWS. 
 - Each AWS account has a public and private registry. Each registry can have many repositors.
 - Each repository can contain many images.
 - Images can have several tags, need to be unique within repository.
 - Public - anyone can have read permissions to, read/write will need granted permissions
 - Private - permissions are needed for both read and write
 - Integrated with IAM - permissions
 - Image scanning, basic and enhanced (inspector, can scan for issues within OS and software packages within containers. Layer by layer.) 
 - Real-time Metrics => CW (auth, push, pull)
- API Actions - Cloudtrail
- Events - EventBridge
- Replication across Regions and cross-accounts