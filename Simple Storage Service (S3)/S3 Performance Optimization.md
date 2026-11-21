
## Personal Notes

 - When an object is uploaded to S3, it is done as a single stream of data. And if that stream fails, then that upload fails and must be fully restarted. "It's just a bad idea."
 - S3 has a speed and reliability limit of 1 stream. 
 - There is a limit of a stream up to 5 GB, "but I would never trust an upload anywhere close to that size"
Multipart Upload:
	- Data is broken up 
	- Minimum data size of 100MB for multipart. 
	- Can be split into a maximum of 10,000 parts, each in size is between 5MB and 5GB.
	- Parts can fail in isolation and be reset in isolation. Risk of upload is significantly reduced. 
	- Transfer rate = speed of all parts, is reduced/improved.

S3 Accelerated Transfer:
	 - Edge locations are hubs in inconvenient places across the world.
	 - To use, an S3 bucket must have Accelerated Transfer enabled; bucket name must not contain periods and be DNS  compatible.
	 - Data being uploaded to an S3 bucket, doesn't bunny-hop between centers, but goes to an edge location, which goes through less normal networks, giving it better performance over public wifi. The edge locations transfer the data over the AWS Global Network, a direct link to the S3 bucket is provided. 
	 - AWS Network is purpose built to link regions to other regions within the AWS network; source to destination, lower, consistent latency and more reliable. 
	 - Larger the distance between sender and receiver, the better the performance and benefit of using S3 Accelerated Transfer.
 