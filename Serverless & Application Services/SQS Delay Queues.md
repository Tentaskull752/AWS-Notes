

 - Allow the postponing of messages to consumers.
 -  VisibilityTimeout is set to a default of 30 secs, though the range  is from 0 secs to 12 hours.
 - Machine iniciating the process may not be able to respond about the failure; so the message will naturally return to the queue.

 - Delay queues hide messages for a selected time. Default is 0 secs, for it to go into effect, it must be a non 0 secs value. Max is 15 minutes. 
 - Delay queue can override any queue settings. 