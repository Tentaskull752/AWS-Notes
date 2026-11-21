

 - Public, Fully managed, highly-available Queues - Standard or FiFo
 - Messages up to 256KB - link to large data
 - When a message is polled from a queue, it doesn't disappear, but is hidden for some time (VisibilityTimeout). Message can be manually deleted though. 
 - Dead-Letter queues ca be used for problem messages; allows processing of different sets of messages that are problems. 
 - ASGs can scale and Lambdas invoke based on queue length. 

Elastic Architecture using SQS Queue:
 - Client send master vid to to the ASG Web Pool
 - Web Pool sends this vid to a dedicated S3 bucket, but also to the queue with a message of the vid's location and size
 - Worker Pool polls the queue to find the master vid in the master bucket and pulls it.
 - Worker pool creates different sizes of the master vid and sends it to a dedicated Transcode bucket
 - The master vid is deleted, and the original master vid message is deleted from the queue. 
 - Size of worker pool ASG scales back in as size of queue decreases. 

 - For the simultaneous creation of different vid sizes from a single master vid:
	 - Use an architecture consisting of SNS and SQS fanout.
	 - A message is still sent, but to a topic, which has it's own followers. There is a queue for the 1080p, one for the 720, and one for the 480.
	 - This message containing the master vid's size and location is sent to each queue, and the three separate worker pools work out their own individual video.
	 - All three videos are then sent to the Transcode bucket, and the original message is deleted from all three of the queues.


 - Standard Queue = at-least-once guarantee, though the order cannot be predicted. Can get the same message delivered twice on the same poll in different values
 - FIFO = exactly-once, put something in first, you are getting it back first.
 - FIFO(Performance) 3,000 messages per second with batching, or up to 300 messages per second without
 - YOU ARE BILLED ON 'REQUESTS'
 - 1 request = 1-10 messages up to 64KB total
 - Short (immediate) vs Long (waitTimeSeconds) Polling
 - Encryption at rest (KMS) & in-transit
 - Queue can only allow access from external accounts, just like a resource policy giving access to the queue. 



FIFO queues have to have a FIFO suffix in order to be a valid FIFO queue. 
 - FIFO is great for in-order processing, workflow ordering, and price adjustments.

 - Standard Queue is ideal decoupling application components, worker pools, and Batch for future processing.