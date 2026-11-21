

## Personal Summary

   - Automated and Snapshots (both in S3) are the two types of backups in RDS.
   - These two used AWS-managed buckets, so they are not visible to you. Though they are visible is RDS.
   - Data stored in S3 becomes REGIONALLY RESILIENT. 
   - Backup is derived from the standby instance, so there are no pauses in performance. 
   - The first snapshot is a full copy of the DB, and any snapshots that follow record changes from the initial batch of data.
   - Snapshot creation will decrease in speed since only changes are recorded.
   - Snapshots are immortal, they will live beyond the RDS deletion, and must be deleted manually.
   
   - If you're using single AZ, make sure the Automated Backup/Snapshot occurs during times of little use. 
   - Automated backups occur once per day; first contains full data, those that follow records changes to that initial data.
   - Every 5 minutes, transactions logs are sent to S3. They store operations that change the database. 
   - A 5 minute period of recovery can be obtained. 
   - Retention of 0 to 35 days can be obtained. Anything past the 35 mark is deleted. 
   
 - RDS can replicated backups/snapshots to another region. Transaction logs as well.
   - Charges apply for the cross-region data copy, and the storage in the destination region.
   - NOT DEFAULT, HAS TO BE ENABLE

 - Restores create a new RDS Instance - new address.
 - Snapshots = single point in time, creation time
 - Automated = any 5 minute point in time
 - Backup is restored and transaction logs are 'replayed' to bring DB to desired point in time
 - Restores aren't fast - Think about RTO