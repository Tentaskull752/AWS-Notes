

 - Provide Authentication(logging in), Authorization(giving permission), and user management for web/mobile apps(managing use and creation of serverless databases)
 - User Pools - Sign-in and get a JSON Web Token (JWT). Do not grant access to AWS resources
 - User directory management and profiles, sign-up & sign-in (customizable web UI), MFA and other security features
 - Identity Pools - Allow you to off access to Temporary AWS Credentials
 - Unauthenticated Identities - Guest Users
 - Federated Identities - SWAP - Google, Facebook, Twitter, SAML2.0 & User Pool for short term AWS credentials to access AWS Resources
 - Identity pools assume an IAM role on behalf of the identity user; generates temp. credentials back to user on a mobile or online application. 


 - Once JWT is swapped for temp credentials (becomes a USER POOL IDENTITY) the identity can access self-managed server based resources and API GATEWAY via Legacy Lambda Custom Authorizers and now directly via API Gateway
 - User Pool passes the JWT to the Identity Pool
 - IDENTITY POOL: takes the external identity provider coin and sends it to an Identity Pool to create temp AWS credentials (Federation). Identity Pool creates two roles for authenticated and unauthenticated identities. Cognito assumes a role and temp. credentials are created, these are sent back to the application, which can then use these credentials to access AWS resources. Once they expire, new ones are created. 