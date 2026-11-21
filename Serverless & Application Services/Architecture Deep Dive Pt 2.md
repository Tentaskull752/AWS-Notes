
 -   Queue: system that accepts messages with ordering (first in first out usually)
 - A video could be stored, and a message is sent to the queue, telling things such as the files location or size. And this message for this file is sent to the front of the queue. 
- An Auto Scaling Group (min of 0, Des of 0, and max of 1337). Has auto scaling policies to decrease or increase instances based on queue length.
- These processing instances poll the queue in order(after the Desired value of instance is set to something more than 0). Once a processing job is done, the item is taken out of the queue and sent to upload. 
- Processing tier can scale to an infinite number of instances based on the queue length. It possesses as a worker-fleet architecture.


 - These processes are called "Microservices". 
 - Upload aka Producer: produce data or messages
 - Consumer aka Processor: digest data or messages
 - There are also Microservices that can do both. 
 - A Microservice is it's own application, with it's own logic, set of rules, and data.

 - Event-Driven Architecture:
	 - Event Producers: Bits of software that generate or produce events in reaction to something else. Error occurs, someone uploads something.
	- Event Consumers: it will take an action based on an event. Dispatch a human to resolve an error, change some data values to resolve a package mis-delivery. Events are delivered, and they take an action, and they then stop. 
	- Event Router: highly available exchange router for events. Determines which events are delivered to which consumers. 
		- Event Bus: Event Producer has an event, it is then put into the Event Bus and taken off to Event Consumers. 