
## Personal Notes

  - Allows creation of event notification configurations in S3 buckets.
  - Can be delivered to SNS, SQS, and Lambda functions
  - Object Created (put, post, copy, CompleteMultiPartUpload)
  - Object Delete (*,Delete, DeleteMarkerCreated)
  - Object Restore(Post(Initiated), Completed)
  - Replication(OperationMissedThreshold, OperationReplicatedAfterThreshold, OperationNotTracked, OperationFailedReplication)

 - The notifications are JSON-coded objects, and are sent to destination either through a Lambda function or SQS queue. 
 - EventBridge is an alternative and supports more types of events and more services.