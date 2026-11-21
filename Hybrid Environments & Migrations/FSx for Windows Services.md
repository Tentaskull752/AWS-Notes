
## Personal Summary

- Provides fully managed native windows file servers/shares. 
- Designed for integration with windows environments
- Integrates with Directory Service or Self-Managed AD. Good because it can integrate with normal AD's that most companies already have.
- Single or Multi-AZ within a VPC
- On-demand and Scheduled Backups
- Files created  within FSx can be accessed using VPC, Peering, VPN, Direct Connect

- Ex. of a file link: \\fs-xxx123.animals4life.org\catpics

- FSx supports resting encryption via KMS, and also encryption during transit.
- Allows shadow copies and allows replicas of a file via OS on the client side.
- 8 Mb to 2 Gb per sec, hundreds of thousands of IOPS, and less than a millisecond of latency.

- VSS - User-Driven (File and Folder) Restores. If there are any of the two on FSx, go to versions and restore without going in as adminstrator
- Native file system accessible over SMB
- Windows Permission Model; used to support Windows Environments in AWS
- Supports DFS .. scale-out file share structure. Can group file-shares together or use DFS for replication or scaling out performance. 
- Managed - no file server admin overhead
- Integrates with DS AND YOUR OWN directory