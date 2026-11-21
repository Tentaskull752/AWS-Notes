
## Personal Summary

- ONLY APPLICABLE TO S3 ORIGINS
- OAI - type of identity
- can be associated with CloudFront Distributions
- CloudFront distribution 'becomes' that OAI
- when a distribution is accessing S3, it gains permissions to operate in S3 Bucket Policies
- Best strat is to lock down the S3 to only be accessed by CloudFront; Deny all BUT one or more OAI's
- Edge location's gain the identity (OAI) that is attached to the distribution; create or adjust bucket policy, add an explicit DENY in the identity, and turn off public access to the S3 bucket. 
- Once OAI is associated with the distribution accesses are FROM the OAI

- Custom origins require Customer Headers; if not present, the custom origin will deny the requests
- Can apply a firewall around IP Ranges which only allows connections from the Edge Locations; ONLY CLOUDFRONT CAN GET THE CUSTOM ORIGIN