
## Personal Summary

- Autonomous System (AS) - Routers controlled by one entity... a network in BGP. Blackboxes that only are concerned about network routing in and out of the system
- ASN are unique and allocated by IANA (0-65535), 64512-65534 are private
- BGP Operates over tcp/179 - it's reliable
- NOT AUTOMATIC - peering is manually configured between the two autonomous systems
- BGP is a path-vector protocol, exchanges the BEST PATH to a destination between peers... the path is called the ASPATH
- IBGP = Internal BGP - Routing within an AS
- eBGP = External BGP - Routing between AS's

 - i is the origin - the network was learned from a locally connected network
 - BGP ALWAYS USES THE SHORTER PATH TO A GIVEN NETWORK
 - Satellite connection is only used as a backup, higher latency and only sends at 5 MB per sec when compared to a Fiber Connection
 - AS Path Pretending can be used to artificially make the satellite path look longer making the fiber path preferred.
 - The AS prepends its own AS number onto the path - creating a source to destination path which BPG routers can learn & propagate. 