
## Personal Summary

- HTTP - simple and insecure; could compromise domain names and data from customers
- HTTPS - SSL/TLS Layer of Encryption added to HTTP
- Data is encrypted in-transit
- Certificates prove identity
- Chain of trust - Signed by a trusted authority
- ACM lets your run a public or private Certificate Authority (CA)
- Private CA - Browsers trust a list of providers, which can trust other providers, establishing a chain of trust

 - ACM can generate or import Certificates
 - If generated, it can be Automatically Renewed
 - If imported, YOU ARE RESPONSBILE FOR RENEWAL
 - Certificates can be deployed out to supported services 
 - Supported AWS Services ONLY (e.g. CloudFront and ALBs...NOT EC2 becase if you have root access, there will always be a way to access the certificates)

 - ACM is a REGIONAL SERVICE
 - Certs CANNOT leave the region they are generated or imported in
 - IF YOU WANT TO USE A CERT FOR AN ALB IN A SPECIFIC REGION, THAT CERT NEEDS TO BE IN THAT SPECIFIC REGION
- Global Services such as CloudFront operate as though within 'us-east-1', SO ALWAYS use Certs for CloudFront in us-east-1 in ACM. The Cert is deployed by ACM to the distribution - then the distribution sends to the edge locations
- Security Admin creates the Certs for the services and IN the region these services are used.