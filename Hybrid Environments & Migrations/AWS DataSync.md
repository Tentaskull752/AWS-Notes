
## Personal Summary

- Data Transfer service TO and FROM AWS
- Migrations, Data Processing Transfers, Archival/Cost Effective Storage or DR/BC
- ....designed to work at huge scale, agent can hand 10 Gbps (-100TB per day) each job can handled 50 million files
- Keeps metadata(permissions/timestamps)
- Built in data validation

- Scalable - can get more agents 
- Bandwidth Limiters (avoid link saturation)
- Incremental and scheduled transfer options
- Compression and encryption
- Automatic recovery from transit errors
- AWS Service Integration - S3, EFS, FSx
- Pay as you use. Per GB cost of data moved

- Datasync Agent runs on a virtualization platform such as VMWare and communnications with the AWS DataSync Endpoint

- Need to have the AWS AutoSync installed on  your local on-premises environment
- Communicates over NFS or SMB with on-premises storage
- Transfers data through to AWS
- Can recover from failures, can use schedules, can throttle bandwidth between on-premises and AWS, can store into S3, Elastic File System or FSx for Windows Servers

- Task- a 'job' within DataSync, defines what is being synced, how quickly, From where and To where
- Agent - Software used to read and write to on-premises data stores using NFS or SMB
- Location - every tasks has two locations, being From and To. Network File System (NFS), Server Message Block (SMB), Amazon EFS, Amazon FSx and Amazon S3