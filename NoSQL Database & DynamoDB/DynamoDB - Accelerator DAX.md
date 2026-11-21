

- It is a service that is installed onto the Instance application
- It cuts out the trouble of pinging a cache and then sadly getting a miss, then going to DB and getting  your answer there and then DB updating it's  cache
- It acts a middle man that gives you a single request; it goes to the cache and DB for you
- Reduces costs heavily for big read jobs

- Works in the form of a cluster, the Read & Write Node, and two Read Replica Nodes.
- Instance connects to the master R&W Node, and this node then connects to DB
- Item Cache: holds all of DAX's data items
- Query Cache: stores items retrieved by query or scan operations, BUT ALSO the parameters used to find and fetch those items

- Each DAX cluster has an endpoint, used to load-balance across the cluster.
- Hits using DAX can be returned within Microseconds, Misses can be done and fixed within single digit milliseconds
- Write-Through: You can write new data to DB THROUGH DAX

- Nodes are HA...primary failure = election for a new Primary Node
- In-Memory Cache - scaling....much faster reads, reduces costs
- Can scale UP and OUT (bigger/stronger and more)
- DAX is deployed within a VPC