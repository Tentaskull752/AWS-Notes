
## Personal Notes

 - Usual access of AWS resources is usually done through API's, a second request for access to such resources.
 - This feature allows access via HTTP
 - Index(default page that is returned to you when you don't ask for anything specific, for ex. Netflix.com) and Error(access a file that isn't there or a server-side error) documents are set. Both need to be HTML-based because static S3 ships in HTML.
 - When you enable this feature on a bucket, a Website Endpoint is created, allowing the reaching of this bucket through HTTP. 
 - BUCKETNAME MATTERS, the domain and bucket name must be the exact same. 
 - Offloading: Domain is linked to an S3 bucket. An animals website has a live top 10 list that is updating constantly, probably going to need a database for this. But images are within that database; move these to S3 bucket, and when the database sends an HTML to the website, it points to the bucket containing the images for the website. 
 - Out-of-Band Pages: A database isn't functioning properly during a maintenance period, we could change the DNS and send traffic to  the static website on the S3 bucket.
 - Storing on S3, it is a PER GIG PER MONTH CHARGE. Sending data( in GB) in or out of S3 also incurs a cost; transferring into S3 is free, transferring out by the GB has a cost. Storing has a cheap price, some of the cheapest. Requesting data also comes with a cost. 
 
