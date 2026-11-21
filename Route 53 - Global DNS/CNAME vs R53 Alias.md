
## Personal Summary

 - An "A" record maps a name to an IP address ex. catagram.io -> 1.3.3.7
 - CNAME maps a name to another name ex. www.catagram.io -> catagram.io. It creates an alternate name for an already existing name.
 - CNAME is invalid for naked/apex (catagram.io)
 - Many AWS services don't give an IP address but instead a DNS Name (ELBs). So the apex existing in the ELB would be invalid
 - ALIAS RECORDS map a NAME to an AWS resource. 
 - Can be used for both the naked/apex and normal records. 
 - For non apex/naked - functions like CNAME
 - For AWS Services - default to picking Alias
 - Should be the same "Type" as what the record is pointing at
 - API Gateway, CloudFront, Elastic Beanstalk, ELB, Global Accelerator & S3.
 - 