

 - Fully managed services that loads data for data lakes, data stores, and analytic services.
 - Automatic scaling ... fully serverless & resilient
 - NEVER REAL TIME DELIVERY (around 60 secs, although it can RECEIVE data in real time. It waits 60 secs (Buffer interval) or delivery when buffer size in MB (1) fill
 - Supports transformation of data on the fly by lambda, can add latency based on complexity of operation
 - Billing - volume through firehose

 - Firehose can deliver to HTTP (3rd Party Providers), Redshift, ElasticSearch, and Destination Buckets. 