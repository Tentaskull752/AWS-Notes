
#### Personal Summary 

   
 - Cloudwatch is a REGIONAL and public service that can be accessed from AWS or on-premises.
 - Store, Monitor and access logging data.
 - Can be integrated with EC2, VPC Flow Logs, Lambda, CloudTrail, R53 and more. 
 - Can take logs and create metrics from it; takes failures and creates metrics to sound alarms when something goes wrong. 
 - Logging sources such as AWS or apps, can input logs into Cloudwatch as Log Events. 
 - Log Streams: A list of log events from the same source. 
 - Log Group: a container of log streams, each representing its own source. It's on the log group where we determine retention and permissions that are distributed to all log streams within it. 
 - Metric filters are created in Log Groups as well; they're scanning for failures or login mishaps, they then create metrics, and when tripped, send out alarms to dev teams. 
