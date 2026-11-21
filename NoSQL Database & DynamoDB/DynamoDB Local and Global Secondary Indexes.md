

- Local Secondary Index: Gives a new/alternative perspective of data in the form of projection (attributes/ keys_only, Include, ALL)
- Uses a different SK with the same PK
- MUST be created with the table, can't be created after table's creation
- 5 LSI's per base table
- Shares the RCU and WCU with the table
- Indexes are sparse, only items which have a value in the index alternative sort  key are added to the 
- Strong Consistency


-  Global Secondary Index: Gives a new/alternative perspective of data in the form of projection
- Uses a different SK and different PK
- CAN be created after table creation
- Up to 20 GLIs per table
- Has it's own RCU and WCU
- Is parse, when queried, items with no attribute wanted within the SK and PK is omitted. 
- Eventually consistent, use by DEFAULT


CAREFUL WITH PROJECTION, everything you bring into index, it brings it's capacity with it