
## Personal Notes

   - A way of logging access to S3 buckets and their objects. 
   - There is a Source bucket and a Target bucket.
   - S3 Log Delivery Group is Best Efforts log delivery, accesses to source bucket are usually logged in the target bucket within a few hours.
   - Access logging can be enabled via the console UI or via PUT Bucket Logging.
   - S3 Log Delivery Group will need and gains access to the target bucket via a Bucket ACL Allow.
   - Once it has access, S3 LDG sends accesses of the source bucket and objects across in the form of log files containing log records, which are newline-delimited, and attributes are space-delimited. 