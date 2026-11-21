
## Personal Notes

 - BUCKETS AREN"T ENCRYPTED, OBJECTS ARE
 - Client-side and Server-side encryption are two methods of encryption in AWS. 
	 - Client-side: objects being uploaded by the client are encrypted into ciphertext before they ever leave for transit.
	 - Server-side(SSE): Even though the data is encrypted in transit, the objects aren't initially encrypted. Once the data hits the S3 endpoint, it is then encrypted. AWS has made encryption at the Server-side mandatory on objects in S3 buckets. 
 - Server-Side Encryption with Customer-Provided Keys (SSE-C): 
	 - Customer provides plaintext object and encryption key. When it arrives at S3, object is encrypted and a one-way hash is created of the key, and original key is destroyed. To decrypt, ask S3 and provide cyphertext along with the key after cyphertext has been put in S3 storage. 
 - SSE-S3(AES256): AWS handles both key generation and management along with encryption of objects and data. When an object is uploaded to S3 endpoint, a key is created for each object, and that object is then turned into a cyphertext immediately.   Using an S3 key(S3 also rotates physical material behind each key, the user has no control), the object key is encrypted into an encrypted object key. Cypertext object and Cyphertext key are left over in S3 storage. 
 
 - SSE-KMS: Instead of S3 managing keys, KMS now takes over this responsibility. You can create this custom and managed KMS key, it has isolated permissions, and is configurable. When S3 wants to encrypt something, it has to ask KMS to give permission with the use of the KMS key. KMS then provide two versions of the encryption key, both a plaintext and a cyphertext key. KMS keys can only encrypt objects up to 4KB in size. KMS doesn't store these keys, only generates them and S3 stores them in S3 storage. Auditing and logging are possible with the KMS and Cloudtrail can be utilized to monitor any actions against it. In order to decrypt an object originally encrypted by SSE-KMS, you will need the KMS key. Someone with only S3 permissions can access the buckets, but can't read the objects as they don't have permissions to the KMS key to decrypt those objects. 