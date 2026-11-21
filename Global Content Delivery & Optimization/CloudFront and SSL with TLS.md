
## Personal Summary

- Each CloudFront distribution receives a Default Domain Name (CNAME)
- Usually ends in "cloudfront.net"
- SSL Supported by default... *.cloudfront.net cert
- Alternate Domain Names (CNAMES) e.g. cdn.catagram... can point this at your CloudFront Distribution using a service such as Route53
- Must Verify Ownership (optionally HTTPS) using a matching Certificate
- MUST generate or import in ACM ...in us-east-1(IN REGION THAT YOU'RE WORKING)
- HTTP or HTTPS, HTTP => HTTPS, HTTPS Only; all these options are available for customers.
- If using HTTPS with CloudFront, you must have the appropriate Cert to go with that name.
- Two SSL Connections: Viewer => CloudFront and CloudFront => Origin (BOTH NEED VALID PUBLIC CERTIFICATES (AND INTERMEDIATE CERTS))

 - Every SSL enabled site needed its own IP
 - Encryption starts at the TCP connection; Host headers happens after that - Layer 7 // Application
 - SNI is a TLS extension, allowing a host to be included; resulting in many SSL Certs/Hosts using a shared IP
 - Older browsers don't support SNI...CF charges extra for dedicated IP

 - Viewer Protocol: Connection by customer to edge locations by using dedicated IP at each CF Edge Location
 - Cert used by Edge Location HAS TO BE PUBLICALLY TRUSTED (Comodo, DigiCert, or Symantec or ACM (us-east-1) Matches the DNS NAME)
- Cert needed to match the DNS NAME assigned with the Distribution
- ONLY PUBLICALLY TRUSTED CERTS ARE ABLE TO APPLIED TO CLOUDFRONT DISTRIBUTIONS

 - Connection oof Origin to the Edge Location is called ORIGIN PROTOCOL
 - MUST POSSESS PUBLICALLY APPROVED CERTS
 - S3 Origins automatically handles Certification needs and you CAN'T change the cert on an S3 bucket
 - ABL NEEDS A PUBLICALLY TRUSTED CERT
 