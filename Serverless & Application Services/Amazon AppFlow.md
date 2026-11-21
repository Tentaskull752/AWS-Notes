

 - Fully-managed Integration service
 - Exchange data between SaaS applications and AWS Services (connectors) using flows
 - Sync data across applications
 - Aggregate data from different sources
 - Public Endpoints, but works with PrivateLink (privacy)
- AppFlow Custom Connector SDK (build your own)
- e.g. contact records from Salesforce > Redshift
- Support tickets from Zendesk > S3
- Low-code/No-code service
- Can get up to 100 GB per flow
- Auto-encrypted is possible but also has public Endpoints
- Connections store configuration & Credentials to access applications
- Connections can be reused across many flows - they are defined separately
- Field Mapping tells Appflow what fields we're interested in from the SaaS applications and where to place them in the AWS Service
- Data Transformation is optional
- Can configure filters and validation