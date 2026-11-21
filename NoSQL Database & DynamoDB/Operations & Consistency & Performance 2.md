

-  Storage Node - replication of data within multiple AZs within the DynamoDB service
- One node is the leader


- Eventual Consistency: the data being imported is not being received by an up-to-date node. Data is eventually synced, not immediately. A read request can check 1/3 of the nodes for ex. and it could have stale info on it. Half the price of strongly consistent
- Strong Consistency: a read request goes directly to the Leader Node and receives the most up-to-date data. 
- Not every application tolerates eventual consistency. 

Ex. store 10 items per second, avg size of each item is 2.5 K.
1 WCU = 1 KB
2.5 K / 1 KB
2.5 WCU -> 3 WCU (rounded)
Multiply by avg number per second (30)
