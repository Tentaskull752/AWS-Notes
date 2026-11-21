
#### Personal Summary 

 - "IAM Users are an identity used for anything requiring long-term AWS access e.g. Humans, Applications or service accounts."
 - 'Principals' is a person or an application  that makes a request to IAM to become authenticated against an IAM identity to interact with resources. 
 - Partitions specify the address of the resource being accessed. For ex. Partition: service: region: account-id: resource-id
 - ARNs: uniquely identify resources within any AWS accounts. If services have similar names between two IAM accounts, they can be properly named/identified using the ARN as reference. 
 - If you want to create a policy to manipulate S3, then you would need two ARNs; one to access the bucket, and another to access the objects within the bucket. 
 - ONLY HAVE 5,000 IAM Users per account
 - IAM User can be a member of 10 groups
 - This is a limit for Internet-scale applications or large orgs & org merges. 
 - IAM Roles & Identity Federation fix this.
 - DO NOT CLICK ANSWER ON TEST SAYING MAKE IAM USERS FOR 5K+ USERS


### Questions and Links

