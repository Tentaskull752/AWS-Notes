
- There are two modes for capacity when making a table in DynamoDB:
	- On-Demand: unknown, unpredictable, low-admin. Price per million R or W units
	- Provisioned:: RCU and WCU set on a per table basis. Every operation consumes at least 1 RCU/WCU(*)
	- 1 RCU is 1 x 4KB read operation per second
	- 1 WCU is 1 x 1KB write operation per second
	- Every table has a RCU and WCU burst pool (300 seconds of the sustained avg of RCU and WCU). Deplete the pool, you will receive a provisioned see-through error and you will throthled

- Query: an operation that can return data from a table containing items, must specify primary key. It accepts a single PK value and optionally  a SK or range. Capacity consumed is the size of all returned items. Can ONLY query on PK or PK & SK
- Query (PK = 1)
- Two items for example, 2.5K and 1.5K = 4K (1 RCU)
- If an item is less than 4KB, it will be rounded 

- Scan: moves through a table consuming the capacity of every ITEM. You have complete control over what data is selected, any attribute can be used and any filters applied but SCAN consumes capacity for every ITEM scanned through