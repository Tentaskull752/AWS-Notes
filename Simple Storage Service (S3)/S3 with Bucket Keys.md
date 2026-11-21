
## Personal Notes

  - KMS has an always rising cost as more and more objects are put into an S3 buckets using the encryption method of SSE-KMS. Throttling occurs, 5,500 or 10,000 or 50,000 p/s across regions. 
  - Instead of creating a unique key for each object, a bucket key exists and is created temporarily by the KMS key. And this bucket key can offload the intensive processing from KMS and reduce costs as this bucket key creates this encrypted object and key pair for storage.
  - Cloudtrail KMS will show less logs as the bucket key will take over object and key encryption(generation); the bucket will show up in the logs instead of the object. 
  - Object encryption is preserved through region and cross-region replication of buckets. 
  - If replicating a plaintext to a bucket using bucket keys the object is encrypted at the destination side (ETAG changes).
  - BUCKET KEYS CAN REDUCE KMS COSTS BY 99%!