

- There is no master table, there are same-level tables across multiple regions across the globe
- Goes on a last-writer conflict resolution; most recent writer has their data sent to the other tables. 
- Has sub-second replication between replica tables when they're connect to the global table service
- Provides Global HA and Global DR/BC
- Global eventual consistency, but same region reads give strongly consistent reads