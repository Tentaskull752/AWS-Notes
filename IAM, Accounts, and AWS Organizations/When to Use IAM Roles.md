
#### Personal Summary 

   - An application or a script running, such as a Lambda function, can be assumed into a role, named Lambda Execution Role. The trust policy allows it, and the permissions policy allows the Lambda certain actions. It then obtains STS rights for a temporary amount of time, "sts:AssumeRole", which then gives it access to AWS services such as Cloudwatch and S3. 
   - Senior teams can give monitoring teams below them viewer rights of services and metrics to ring the alarm when there's an emergency. BREAK THE GLASS allows rights to services when there is an emergency.
   - EXTERNAL ACCOUNTS CAN'T BE USED IN AWS DIRECTLY
   - Existing roles existing on on-premises servers can access roles within AWS to then be granted access to acting upon AWS services such as S3 buckets.
   - Web Identities, such as google, facebook, or twitter can log you into an app and the user will then assume a role to access an AWS service directly through the app. Using ID Federation, this utilizes pre-existing accounts, and this can be used for 100,000.000's
   - Cross-account access allows identities in one AWS account, to access services in a partner account through the second account setting up a role to grant access to that service. The partner account still owns that role. You don't need to assign permissions or login to those identities within the first account.



### Questions and Links

