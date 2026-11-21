
## Personal Notes

 - Simplify managing access to S3 buckets/objects.
 - Rather than 1 bucket w/ 1 complicated bucket policy; Create many access points with different policies, each with different network access controls. 
 - Each access point has its own endpoint address.
 - Created via console or aws s3control create-access-point
 - Access points can be thought as mini-buckets; if there is admin staff, field workers, and vet staff, an access point can be given to each group and the VPC resources as well. 
 - Access points control permissions for access via the access point & is functionally equivalent to a bucket policy. 
 - Access point policy can restrict identities to certain prefix(s), tags, or actions based on need. 
 - Each Access Point has a unique DNS address for Network access. 
 - Access Points can be configured for access via a VPC - requires a VPC endpoint. Access via this route can be enforced by endpoint policies.
 - Access point w/ VPC Origin can fill the role of a Bucket Policy.
 - Can create up to 10,000 access points per Region per AWS account. If you need more, you can request for more via a service quota increase.
 - You can also create a cross-account access point that's associated with a bucket in another AWS account, as long as you know the bucket name and the bucket owner's account ID. However, creating cross-account access points doesn't grant you access to data in the bucket until you are granted permissions from the bucket owner.