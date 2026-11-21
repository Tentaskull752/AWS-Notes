
 - Is a consolidation of backups from many AWS services such as EC2, VMWARE, EBS, EFS Aurora, RDS, Neptune, Dynamo DB, and S3.
 - It is fully data-protected for all of these backups.
 - Backup plans - frequency (how often backups are taken for certain products; point-in-time restore feature), window (when a backup occurs and the duration of that backup window), lifeycycle (define when a backup is transition is sent to cold-storage(min of 90 days) and when it expires), vault (), region copy (can copy backs from one region to another)
 - Resources - what resources are backed up
 - Vault - Backup destination (container) - assign KMS key for encryption
 - Vault Lock - write-once, read many (WORM), 72 hour cool off, then afterwards, nobody can delete anything from the vault, even AWS. 
 - On-Demand - manual backups created as needed
 - PITR - Point in time recovery