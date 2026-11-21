
## Personal Summary

- 304 Not Modified, version of object in edge location cache is the current version in the s3 origin
- 200 OK, object in the edge location is not current to the one in the origin; new version from origin is sent to the cache and this is then sent to the customer. 

-  More frequent Cache Hits = Lower Origin Load
- Default TTL (Time To Live) = 24 hours (validity period); objects expire after 24 hours of being cached by edge location
- Mix TTL and Max TTL can be set, if not set, the default 24 Hour will be used
- Origin Header: Cache-Control  maxage(seconds). 
- Origin Header: Cache-Control s-maxage(seconds). Setting either of these will do the same thing, setting the second amount of TTL for an object
- Origin Header: Expires (Date & TIme)
- IF THE MIN TTL IS SET BELOW THE PER OBJECT TTL, THE MIN WILL BE USED; SAME WITH THE MAX TTL.
- Custom Origin or S3 can be used to set these headers (via object metadata)

 - Cache Invalidation ... performed on Distributions
 - ....applies to all edge locations ...takes time
 - It expires all edge locations within that distribution; immediately expires any object despite their set TTL.
 - /* this star means anything on every edge location within the distribution will be expire. 
 - To expire versions or individual files: using Versioned File Names...whiskers1_v1.jpg // _v2jpg 
