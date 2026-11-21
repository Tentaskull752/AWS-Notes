
## Personal Notes

 S3 Glacier - Instant: 
  - Used for long-lived data, accessed infrequently (once per qtr)
  - Per GB data retrieval fee, overall cost increase with frequent data access.
  - Minimum 90 duration charge of 90 days.
  - Min. capacity charge of 128KB per object.
  - Same durability, zones, and checks as standard

S3 Glacier - Flexible:
 -   Same durability, zones, and checks as standard.
 - Storage cost of 1/6th the cost of Standard. 
 - Objects are "cold", meaning they aren't readily available. The stored "objects" are just pointers to the real thing and permission will be given upon retrieval request. Objects are not permanently accessible. 
 - Expedited(1-5 mins), Standard(3-5 hrs), Bulk(5-12 hrs); Faster retrieval = more expensive. 
 - First byte latency = minutes or hours.
 - It is for storing archive data where frequent or daily retrieval isn't needed.
S3 Glacier - Deep Archive
 - Same durability, zones, and checks as standard.
 - Objects are in a "frozen" state. Objects are not publicly accessible, only given through a retrieval request.
 - Much longer retrieve times; Standard (12 hrs), Bulk (up to 48 hrs)
 - First byte latency = hours or days
S3 Intelligent-Tiering
 - Five level of tiers: Frequent access, infrequent access, archive instant access, archive access, and deep archive. 
 - Monitors access frequency for each object and moves an object into one of the five tiers on its own. You can set the amount of days of inactivity needed to move an object into a lower-activity tier. 
 - "Intelligent tiering has a monitoring and automation cost per 1,000 objects. The frequent access tier costs the same as S3 Standard, the infrequent the same as Standard-IA. Archive Instant, Archive and Deep Archive are comparable to their S3 glacier equivalents."
 - S3 Intelligent Tiering should be used for long-lived data with changing or unknown patterns. 
