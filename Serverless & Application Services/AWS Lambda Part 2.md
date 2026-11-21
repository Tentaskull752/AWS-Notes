

 - Public Networking:
	 - By default, Lambda functions are given public networking. It can access public AWS services and the public internet
	 - Public networking offers the best performance because no customer specific VPC networking required
	 - NO ACCESS WITH SERVICES WITHIN VPC (if on default of public networking) UNLESS PUBLIC ADRESSING IS PRESENT IN VPC AND SECURITY

 - Private Networking:
	 - Lambda functions running in a VPC, they obey all VPC networking rules
	 - Can access other VPC-based services. 
	 - Cannot access outside public network services or internet. 
	 - Attachment of a VPCEndpoint or a NATGW pointing to an IGW would be needed to roam outside the VPC. 
	 - Each Lambda Function (in the old style of architecture) used to need a unique ENI for each system that it connected to as they functions existed in their own VPC. 
	 - NOW, the functions in their own vpc, all connect to a single ENI, by possessing the same SG's for the subnets containing the lambda functions, so they all funnel to one spot, which then connects to the other VPC. 


- Execution role exists within the runtime environment, the lambda function possesses this role, and the code is allowed to utilize these permissions. 
- It has a trust policy that trusts lambda, and a permissions policy to generate temp. credentials to interact with other resources. E.g. extract data from Dynamo DB and send it to an S3 bucket. 
- Lambda resource policy controls WHAT services and accounts can INVOKE lambda functions.

 -  Lambda uses CloudWatch, CloudWatch Logs & X-Ray
 - Logs from Lambda executions - CloudWatch Logs
 - Metrics - invocation success/failure, retries, latency etc... are stored in CloudWatch
 - Lambda can be integrated with  X-Ray for distributed tracing (need to trace the path of a user or session through a serverless application utilized Lambda)
 - For Lambda to log into CloudWatch Logs, it requires permissions via the Execution Role