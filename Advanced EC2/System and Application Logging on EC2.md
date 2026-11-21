
## Personal Summary


 - Neither CloudWatch (metrics) or CloudWatch Logs (logging data) can see visible data within an EC2.
 - CloudWatch Agent is required for this, as it sends data from the EC2 to CloudWatch and CloudWatch Logs via granted permissions. 
 
 - Installs CloudWatch Agent within the EC2
 - Configures Agent with "Agent Config"
 - Create an IAM Role with permissions to interact with CloudWatch and CloudWatch Logs.
 - Attach role to EC2 Instance, giving anything on it the same permissions. 
 - Data recorded by Agent because of configuartion, is sent to CloudWatch Logs in the form of Log groups.