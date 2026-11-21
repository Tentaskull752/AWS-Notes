

- Allows a per-item timestamp that allows a data item within a table/partition to be automatically deleted.
- Must enable TTL in a table and select an attribute to use for TTL
- Time is going to be in seconds, must put this value in for this attribute
- A per-partition is periodically run to check current time(sec) for items to be deleted. If the time of an item/attribute is older than the allow TTL, it's removed and deleted
- Best for sensitive data that needs to be cycled/deleted after efficient use