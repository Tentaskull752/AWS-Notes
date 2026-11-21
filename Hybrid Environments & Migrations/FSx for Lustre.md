
## Personal Summary

- Managed Lustre - Designed  for High-Powered-Computing - Linux Clients (POSIX)
- Machine learning, BIG Data, Financial Modeling
- 100's GB/s throughput & sub millisecond latency

- Scratch:
	- Highly optimized for SHORT TERM no replication & fast
- Persistent: 
	- Longer term, HA (in one AZ), self-healing (any failures are auto-replaced by AWS)
- Accessible over VPN or Direct Connect

- File System is where data lives as it waits for processing to occur.
- Can associate with a repository (AN S3 BUCKET). Objects can be viewed in the connected file system.
- Data is 'Lazy Loaded' from S3 into the file system AS IT"S NEEDED. NO BUILT IN SYNCRONIZATION. 
- Data can be exported back to S3 at any point using hsm_archive. 

- metadata(file name, timestamps, permissions) stored on Metadata Target (MST); file system has one of these
- Objects are stored on called object storage targets (OSTs) (1.17TiB); performance levels of lustre achieved by attaching objects between multiple OSTs.
- Size - min 1.2 TiB then increments of 2.4 TiB
- For Scratch - Base 200 MB/s per TiB of storage
- For Persistent - 500 MB/s, 100 MB/s and 200 MB/s per TiB of storage
- Burst up to 1,300 MB/s per TiB (credit system); you earn credits when you use a performance level below your baseline, that you can use to burst above the baseline

- Any FSx architecture uses a client-managed VPC. Something personally designed and implemented. 
- File system will deploy storage servers; will handled to storage requests coming into the system; AND provides a temporary cache
- MORE STORAGE PROVISIONED, MORE SERVERS AND AGGROGATE DELIVERED INTO VPC BY A SINGLE ELASTIC NETWORK INTERFACE
- Path: EC2, ENI, Storage Server, Storage Volume and REVERSED. Once images pass through Storage Servers, caching can be used to pull data instead of from the servers.

- Scratch is designed for pure performance; short term or temp workloads. NO HA and NO REPLICATION
- Larger file systems mean more servers, more disks and MORE CHANCE OF FAILURE!!!'

- Persistent has replication with ONE AZ only; auto-heal and data won't be lost in one AZ
- Both Scratch and Persistent can perform backups & automatic backups via connected S3 buckets.

- ANY MENTION OF LUSTRE, HIGH POWER, MACHINE-LEARNING OR BIG DATA, SAGEMAKER AND NEED FOR  IT'S FSX FOR LUSTRE!!! A REALLY HIGH-PERFORMACNE FILE SYSTEM, LUSTRE AGAIN!!!!