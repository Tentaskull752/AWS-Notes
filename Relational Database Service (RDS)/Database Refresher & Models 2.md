

## Personal Summary

 - DATABASE TYPES FOR NON_RELATIONAL
	- Key-Value, records time (key) and a value (for ex. cookies eaten); no real schema or structure. No tables and no table relationships. Scalable and REALLY Fast. Value could be text, JSON, or a cat picture.
	- Wide Column Store
		- Partition Keys and other keys (secondary keys known as Sort or Range key). Offer grouping of items known as tables (NOT THE SAME AS RELATIONAL). Items within the grouping do not need to be the same attribute. Every item has to use the same key structure, and each must be unique. 
	 - Document
		 - Works for Orders and Contacts databases, can interact with the data through the database. Ideal Scenario: interacting with whole documents or deep attribute interactions. 
	 - Column
		 - Row Store (MySQL): for every order, you have a row. An order comes attributes and values, product, color, size, and price for example. Ideal if operating with adding, updating, and deleting. Auditing, contact, and stock databases. 
		 - Column (Redshift): everything is in a column structure. Very inefficient for transaction style processing. Very good for reporting or when all values for a specific attribute are required. 
	 - Graph
		 - Nodes aka nouns aka objects. Nodes can have properties, basic key values of data that are attached to each node. Edgers have a name and a direction, show relationships between nodes. Jeff, works at Target, located in Michigan. Edgers can also carry data with them, for example, a date. When looking to take advantage of these fluid relationships, use a graph database. 
		
	