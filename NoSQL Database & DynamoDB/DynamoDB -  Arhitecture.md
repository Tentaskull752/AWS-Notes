

- NOSQL Public Database-as-a-Service(DBaaS) - Key/Value & Document data
- Tables are the base entity
- Very fast service, single digit millisecond access to your data, utilizes SSD
- Non Self-managed service
- Highly available across AZs, optionally global
- Backups, point-in-time-recovery, encryption at rest
- Event-Driven integration....do things when data changes

- A Table is a grouping of items with the same primary key. Each Item must have the same primary key and unique values
- Simple (partition) or Composite (Partition & Sort) Primary Key
- Each item MUST have unique value for PK and SK
- Can have none, all, mixture or different attributes (DDB has no rigid attribute schema)
- Item Max is 400KB

- On-Demand Backup: Full copy of table (Retained until Removed)
- Restore: Same or cross-region, with or without indexes, adjust encryption settings

 - Point-in-time-Recovery: must enable, off by default. Provides continuous record of changes, allowing replay to any point in the window of 35 days. Has a 1 second granularity

- NOSQL...preference DynamoDB in the exam
- Relational Data....generally NOT DynamoDB
- Key/Value...preference DynamoDB in the exam
- Access via console, CLI, API...'NO SQL'
- Billed based RCU(1 = 4 KB), WCU (1 = 1KB), Storage and features