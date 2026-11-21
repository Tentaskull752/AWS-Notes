

## Personal Summary

 - Allows Aurora to have multiple instances that can perform both read and write.
 - "Multi-master" instead of "single-master"
 - Cluster Endpoint is used to write, read endpoint is used for load balanced reads.
 - In Multi-Master mode, all instances are R/W
 - There is no load balanced endpoint for the cluster, an application can initiate connection to one or all instances within the cluster. 
 - Once an instance receives a write request for some data, it commits it to all other storage nodes within the cluster. 
 - Each node in the cluster's storage, either accepts or rejects the change in the data. 
 - The write instance is looking for a group of nodes to agree to then write that change to the storage. 
 - That change is then replicated across all nodes in the cluster.
 - But in Multi-master, the change is shared to other nodes as well; so the in-memory cache within the instances are updated and in-sync.
 - Aurora Multi-master write system is nearly fault-tolerant as the connection to multiple writers, each being in-sync and sending any future operations to the others in the case of failure, creates a strong and reliable system against faults within the cluster. 