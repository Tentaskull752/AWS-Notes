
## Personal Notes

 - S3 Standard: 
	 - the default storage class; Bob can store his pics of S3, the objects are then replicated and stored on at least 3 availability zones within the AWS region. 
	 - Possesses 11 9's of storage, meaning for 10,000,000 objects, 1 object loss per 10,000 years. 
	 - Content-MDS Checksums and Cyclic Redundancy Checks (CRCs) are used to detect and fix any data corruption. 
	 - Once objects/data are stored durably, a HTTP/1.1 200 OK code will be provided(REMEMBER FOR TEST) 
	 - Billed GB/m fee for data stored. Transfer IN is free but it's $ per GB Transferring OUT; and a price per 1,000 requests. No specific retrieval fee, no minimal duration, no min. size. 
	 - S3 Standard should be used for frequently accessed data that is important and non-replaceable. 

 - S3 Standard-IA(Infrequent Access):
	  - Data is still stored over 3 AZs, same number of 9's, CRCs and MDS Checksums used to detect corruption.
	  - Storage cost is much cheaper than Standard, about half the price. 
	  - Free Transfer IN and $ per GB for Transfer OUT. For every GB retrieved, there is a fee. Overall cost increases with constant data access. Has a min. charge of 30 days; objects can be stored for less, but the minimum billing applies. 
	  - Should be used for long-lived data that is important, and access is minimal.
 - S3 One Zone-IA: 
     - Retrieval fee, min duration charge of 30 days, and has a min. capacity charge of 128 KB per objects.
     - MULTIPLE COPIES OF PICS/DATA ONLY STORED IN ONE AL; also gets 11 9's of durability IF the AZ doesn't fail. 
     - For data that is non-critical and can be easily replaced and access is infrequent. DON"T USE FOR IMPORTANT, FREQUENTLY ACCESSED/CHANGED, OR IRREPLACABLE.