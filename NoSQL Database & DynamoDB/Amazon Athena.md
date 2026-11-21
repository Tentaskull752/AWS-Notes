

- It is a serverless querying service, that takes pre-loaded data from S3 and has parameters to direct this data into desired table templates. 
- SCHEMA-ON-READ, presents unstructured data is if it's structured data in a database
- Good for Occasional queries on data in S3
- It is cost-conscious since it's a serverless service
- Ideal for querying AWS logs - VPC Flow Logs, CloudTrail Logs, ELB Logs, cost reports
- AWS Glue Data Catalog & Web Server Logs
- w/ Athena Federated Query ...can query other data sources beside S3
- HAS NO INFRASTRUCTURE: NO NEED FOR BUILDING TABLES, DATA MANIPULATION, OR GATHER DATA BEFOREHAND