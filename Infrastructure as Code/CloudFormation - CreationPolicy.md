
-  A Create_Complete state will be present long before the bootstrapping is complete, but how will we know that everything went over good?
- Configure CloudFormation to HOLD/WAIT for a certain # of success signals. 
- Wait for Timeout H:M:S for those signals (12 hour max)
- If wanted success signals is received, status of resource changes into Create_Complete. And Configuration continues. 
- If failure signal received ... creation fails 
- If Timeout is reached....Creation fails
- CreationPolicy or WaitCondition

- CFN-signal runs on resources as a part of the bootstrapping process, where an EC2 instance for example, will send an OK signal, each instance signals once.
- Information can be passed back to CloudFormation within the signal response; a PreSigned URL for resource signals. 
- ![[Pasted image 20260219184734.png]]