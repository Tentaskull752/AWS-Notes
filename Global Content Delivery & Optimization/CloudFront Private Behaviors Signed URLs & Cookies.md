
## Personal Summary

- Public - Open Access to Objects (CloudFront)
- Private - requests require Signed Cookie or URL (CloudFront)
- 1 Behavior - Whole distribution Public or Private
- Multiple Behaviors - each is Public or Private
- OLD - A CloudFront Key is created by an Account Root User
- OLD - THE ACCOUNT is a added as a Trusted Signer
- NEW - TRUSTED KEY GROUP(S) ADDED AND ARE LOGGED AS TRUSTED SIGNERS
- These keys can be managed with the CloudFront API 

 - SignedURLs provides access to ONE OBJECT ONLY
 - Historically RTMP distributions couldn't use cookies
 - Use URL's if your client DOESN"T SUPPORT COOKIES
 - Cookies provide access to groups of objects
 - Use for groups of files/all files of a type - e.g. all cat gifs
 - Or if maintaining application URL's is important

 - 