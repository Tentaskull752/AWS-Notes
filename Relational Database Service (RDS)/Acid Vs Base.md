

## Personal Summary

 - Both are DB transaction models. 
 - CAP Theorem - Consistency (every read to a DB will receive the most recent write or it will get an error), Availability (every request will receive a non error response, but without the guarantee that it receives the most recent write.), Partition Tolerant (system can continue operating even if a single or multiple messages are being dropped between nodes in the network.) ONLY 2 ARE POSSIBLE AT A TIME. 
 - ACID = Consistency]
	 - transactions are atomic, consistent, isolated, and durable. 
	 - IF ACID IS MENTIONED, ITS PROBABLY TALKING ABOUT RDS DATABASES THAT ARE GENERALLY ACID BASED. Acid restricts the ability of a DB to scale. 
	 - Atomic - either all parts of a transaction are successful, or none of the parts are successful. 
	 - Consistent - Transactions move the database from one valid state to another (nothing in between)
	 - Isolated - if multiple transactions occur at once, they don't interfere with each other. Each executes as if it's the only one (doesn't change the state)
	 - Durable - Once committed, transactions are durable. Stored on non-volatile memory, resilient to power outages or crashes.
	 - IF TEST MENTIONS NOSQL OR DYNAMODB, IT MAY BE DYNAMOTRANSACTIONS AS ACID WORKS PRIMARILY WITH RDS
 - BASE = Availability 
	 - Basically available - READ and WRITE operations are available 'as much as possible' but without any consistency guarantees. 
	 - Soft State - database doesn't enforce consistency, this is offloaded onto the application/user. 
	 - Eventually Consistent - If we wait long enough, reads from the system will be consistent. 
	 - NOSQL OR DYNAMO DB
	