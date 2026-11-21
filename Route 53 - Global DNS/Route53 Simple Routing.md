
## Personal Summary

 - A record ex. "A" Record can possess multiple values. If there is a query within a public hosted zone, the "A" record could point www names to multiple IP addresses.
 - If someone sends a query from a laptop to the zone for www, it will be given all of the IP addresses, it will then be sent to a server containing one of those values to access what is needed. 
 - Simple Routing does not support health checks - all values are returned for a record when queried. 