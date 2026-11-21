
## Personal Notes

S3 IS PRIVATE BY DEFAULT, ONLY THE ACCOUNT ROOT USER HAS INITIAL ACCESS TO THE SERVICE AND ITS RESOURCES

  - A bucket policy is a resource policy; like identity policies, but attached to a bucket. "Who can access that resource?"
  - While you can only grant access to an identity within your account; resource policies allow the granting of access to an identity/account outside of your own account.
  - ALLOW/DENY Anonymous principals: can open a bucket to the world, by referencing all principals, even those not authenticated by AWS. 
  - A resource policy statement possesses a "Principal" component that says "which principals are effected by the policy". "If it's there, it's a resource policy."
  - This wildcard/* allows anyone to access object/account/identity within an S3 bucket. 
  - A "Condition" component can be added to block out everyone except someone with a specific IP address for example. Or a deny of accessing the entire bucket unless the user is using Multi-Factor Authentication
  - Access Control Lists(ACLs):
	  - ACLs on objects and bucket
	  - A subresource
	  - They are legacy and AWS doesn't recommend using them outright.
	  - Inflexible and simple permissions. You can't have a single ACL that effects multiple objects. 
 - Block Public Access can deny access to the public or anonymous even if the "access to public" was previously selected. 
 - NEVER USE ACLs UNLESS YOU MUST