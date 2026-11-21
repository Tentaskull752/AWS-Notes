
- Data Security & Data Privacy Service
- Discover Monitor & Store data...stored in S3 buckets
- Automated discovery of data i.e PII, PHI, Finance
- "Will know what it has, what's it in, and where it is"
- Managed Data Identifiers - Built-in - ML/Patterns (used to detect all common types of data within organization)
- Customer Data Identifiers - Proprietary - Regex(certain pattern or text with IDs or performance reports) Based. Can look for specific data
- Discovery Jobs - use identifiers and to find matching items within buckets, creating "findings" or finding events, which  can be view interactively or used as integration with other AWS services.
- Discovery Schedule: when an discovery jobs runs and how often it runs against S3 buckets
- Centrally managed...either via AWS ORG or one Macie Account inviting
- Findings can be  sent to Eventbridge which is connected to Lambda, leading to event-driven remediation, performing some kind of automatic fix based on the data findings. 


- Policy Findings - policies within a bucket is changed to decrease encryption/protection of said bucket after Macie is activated
- Sensitive Data Finding - discovers sensitive data  within S3 objects that you configured it to search
- Policy: IAMUSER/S3BlockPublicAccessDisabled (EXAMPLE OF POLICY FINDING)
- Sensitive: S3Object/Credentials, SensitiveData:S3Object/CustomIdentifier, SensitiveData:S3Object/Financial 