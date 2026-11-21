
## Personal Summary

- Provide private access to services (S3 and DynamoDB); allow a private only resource inside a VPC or any resource within a private only VPC to access S3 or Dynamo DB
- Allows the access of these public services without public infrastructure. 
- Prefix List added to route table => Gateway Endpoint
- Prefix List uses Gateway Endpoint as target; it represent S3 or DynamoDB (It's like a list of IP's that these services use)
- Gateway Endpoint does not go into a particular subnet or an AZ; it's a HA in a region by default
- In the Gateway Endpoint, you set which subnets would be associated with it and it automatically configures the route. DOES NOT GO INTO A PARTICULAR SUBNET
- Endpoint Policy is used to control what it can access(can restrict access of S3 to only certain buckets)
- Regional....can't access cross-region services 
- Prevent Leaky Buckets - S3 Buckets can be set to private only by allowing access ONLY from a gateway endpoint
