
## Personal Summary

- If you have multiple origins within a distribution, you can group them together into an Origin Group. This provides resilience across those origins. 
- TYPES: S3 buckets, AWS media-package channel endpoints, AWS media-store container endpoints, webservers(custom origins, have different restrictions).
- Origin Access: ability to restrict access to an S3 Origin, except only through a CloudFront Distribution
- Best practice is to select the latest SSL protocol offered by the protocol policy for best protection
- Distribution Protocol and Origin Protoc[[CloudFront and SSL with TLS]]ol must be matched
- Custom Ports must be accompanied by Custom Protocols