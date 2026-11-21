
## Personal Summary

- Customers further away from your storage resources, they go through more "hops" and their route is more indirect, and their service takes a hit. 
- Global Accelerator edge locations starts with 2 x anycast IP Addresses; multiple devices can use an anycast IP.
- Anycast IP's allow a single IP to be in multiple locations. Routing moves traffic to closest location. Send the customer to the nearest global accelerator
- Traffic initially uses public internet & enters a Global Accelerator edge location
- "We move the AWS Network closer to the customer"
- From the edge, data transits globally across the AWS global backbone network. Less hops, directly under AWS control, SIGNIFICANTLY BETTER PERFORMANCE
- The Global Accelerator, once it has obtained customers through the anycast IP's, it then send the users into our network infrastructure.
- CloudFront moves MEDIA closer to the customer, while Global Accelerator moves the NETWORK closer to the customer.


 - Connections enter at edge .. using anycast IPs
 - Transit over AWS backbone to 1+ locations
 - Global Accelerator is a NETWORK PRODUCT; Can be used for NON HTTP/s (TCP/UDP) - **Difference from CloudFront
 