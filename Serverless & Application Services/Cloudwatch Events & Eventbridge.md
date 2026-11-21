

 - Allow the implementation of architecture that records "if x happens, or at y times, then do z". 
 - Eventbridge is CloudWatch Events v2.
 - A default Event Bus for each AWS account (implicit, ONLY ONE). 
 - EventBridge can have additional event busses
 - Rules match incoming events on the buses (or schedules) and then deliver those events to a specific target(s). E.g. to invoke a specific Lambda function
 - Two types of rules are Event Pattern Matching Rule and Schedule Rule; when a rule is executed, the event(s) are sent to their designated targets.