
## Personal Notes

 - It is something that you enable for new buckets, not easily do-able for pre-existing buckets.
 - Once enabled, cannot disable, and versioning is enabled as well.
 - Write-Once-Read-Many (WORM) - No Delete, No Overwrite for objects
 - Requires versioning: individual versions are locked
 - 1 - Retention Period:
     - Specify Days & Years
     - Compliance - Object can't be adjusted, deleted, overwritten. Time of retention period, nor the mode, can be changed or deleted at all, even by the root user of the account. Must wait until retention period expires, DONT UNLESS YOU MEAN IT
     - Governance - special permissions granted allowing lock settings and object versions to be adjusted 
     - "s3:BypassGovernanceRetention"
     - "x-amz-bypass-governance-retention:true" (NEED THIS HEADER)
     - Legal Hold - RETENTION PERIOD IS SET AT ALL. For an object version, you set it ON or OFF. No deletes or changes until removed. s3:PutObjectLegalHold is required to add or remove. Prevent accidental deletion of critical object versions.
 - 2 - Legal Hold
 - Both, One, or the other, or none
 - A bucket can have default Object Lock Settings