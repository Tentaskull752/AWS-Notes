

 - Scalable streaming service, meant to ingest a lot of data from lots of different devices.
 - Producers send data into the kinesis stream.
 - Can scale from low to nearly infinite data rates
 - Public service & highly available
 - Streams store a 24-hour moving window of data. The window can be increased to a max of 365 days. 
 - Multiple consumers access data from the moving window. 

 - Kinesis scales by using Shard Architecture. Each shard has 1 MB of ingestion and 2 MB of Consumption. The more data shard takes in, the more expensive it is. 
 - Kinesis Data Record (1 MB) - stored across shards, performance scale linearly based on # of shards.
 - Data Firehose - can move data from the Kinesis Stream in mass to another AWS service such as S3. 


SQS vs Kinesis: 
 - "Ingestion of data" = Kinesis
 - Decoupling or asynchronous communication = SQS 
 - SQS generally has one thing sending something to the SQS queue, and one consumer getting that data.
 - Decoupling and Asynchronous communications (sender and receiver don't know nor care about each other)
 - No persistence of messages, no window within SQS queues. 
 - KINESIS IS DESIGNED FOR HUGH SCALE INGESTION OF DATA
 - Kinesis has multiple consumers...rolling window
 - Data ingestion, analytics, monitoring, App Clicks