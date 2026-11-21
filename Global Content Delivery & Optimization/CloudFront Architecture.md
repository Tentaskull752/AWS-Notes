
## Personal Summary

- Origin - Source location of your content
- Distribution - the 'configuration' unit of CloudFront
- Edge location - local cache of your data
- Regional Edge Cache - Larger version of Edge location. Provides another layer of caching, hold more data that is accessed less frequently, gives a performance benefit due to caching near customers. 
- A domain name is given to each distribution and they are unique; will end in cloudfront.net. Can take your personal domain name and configure the distribution to use that instead. 
- Cached Hit = edge location cache has the item that someone requests.
- Cached Miss = edge location cache doesn't have the item that a customer wants, request then goes to Regional Edge Cache (bigger library). 
- Origin Fetch = if the item is not in the Regional Cache, then content is fetched from the origin, the object is then stored on the Regional Cache, and then the Regional Cache pushes it out to the Edge location. Giving her a cache hit.
- Cloudfront integrates with AWS Certificate Manager for HTTPS, can use SSL certificates.
- Cloudfront is Download Style Operations ONLY. Any uploads go straight to the origin for processing. No-Write-Caching

 - Behavior - a configuration within a Distribution. 
 - Origins are used by behaviors as content sources. THE BEHAVIOR LINKS THE ORIGIN AND DISTRIBUTION-CONTAINING CACHES
 - A Distribution has a Default Behavior, but can have many more. 
 - Accessing a certain object or private objects can bring with it security protection. So a behavior could say that anything accessed possessing a path of (img/*) would be sent through "Private Behavior #1". 
 - Different configurations can be assigned to this path. Origins, Origin groups, TTL, Protocol Policies, restricted accesses are configured vs Behaviors. 