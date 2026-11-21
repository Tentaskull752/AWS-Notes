
## Personal Summary

- "If you see volumes mentioned in the exam, default to volume gateway. If you see anything about tapes, default to VTL Mode. If  you see files mentioned, default to Files mode."
- Bridges on-premises file storage and S3
- Mount Points (shares) available via NFS or SMB.  
- These Mount Points made in  the file gateway, MAP DIRECTLY ONTO A S3 BUCKET
- Files stored into a mount point, are visible objects in an S3 bucket
- Read and Write Caching ensure LAN-like performance

- 1 FileShare(acts as a virtual product) within a File Gateway, is connected to an S3 bucket, and this combination is  called a Bucket Share.
- Files on-premises map directly onto objects within the  S3 bucket. 
- The only thing stored locally is on the local cache. Designed to improve performance to the level of resources running on a LAN
- Anything that can access S3, such as Lambda, allows storage of files via File Gateway. 
- You can create a second server connected to a second File Gateway, and when a file is imprinted onto S3 by the first File Gateway, it can be transported onto the second FG by S3.
- This imprinting is done by a "listing". Although the creation of a file within the first File Gateway creates a most recent version of the file into S3, that file isn't automatically placed into the second File Gateway until a manual listing is completed. 

- File Gateway doesn't support Object Locking - use read only mode on other shares  or tightly control file access
- A second bucket in another region could be created and cross-region replication could be enabled for cross-region DR. 
- These files/objects can be moved throughout S3, S3 Standard IA, and S3 Glacier based on frequency of access to decrease costs of the files existing on S3.