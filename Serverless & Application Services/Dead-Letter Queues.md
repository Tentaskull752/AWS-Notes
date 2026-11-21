

 - Help to handle reoccurring failure while processing other messages. 
 - Every time the message is received, it is recorded. 
 - Redrive policy: specifies the Source Queue, the Dead Letter Queue, and the conditions where messages will be moved from the first to the second.
 - When ReceiveCount > MaxReceiveCount & message isn't deleted, it's moved into the Dead-Letter Queue.
 - All SQS queues have max lifetimes, and if the time a message has been a queue has passed this max lifetime without being processed, it is dropped.
 - Endqueue Timestamp (tells of one a message was added) of message is unchanged. So the timestamp of when the message was moved to the dead-letter queue isn't recorded; dead-letter timestamps are longer than those within the main source queue.
 - A single Dead-Letter Queue can be used for multiple Main Source Queues.