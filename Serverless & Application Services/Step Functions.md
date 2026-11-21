

 - Step Functions address some negative design decisions with Lambda
 - The problem of Lambda being Faas and having a life of 15 minutes, though you can have one invoke another at it's death, but this can get messy at scale. 
 - Runtime Environments are stateless, you cannot hold a state by creating this lambda chain 

- State Machine
	- serverless workflow . Start > States >End
	- States are THINGS which occur; they all take in, modify, and put out data. Can do and decide things as well.
	- Max Duration: 1 year
	- Standard Workflow:
	-  Started via API Gateway, IOT Rules, Eventbridge, Lambda, or Manually
	- State machines are usually used for back-end processing; can also be created via template (JSON-based) in an AWS Service called Amazon State Language (ASL)
	- IAM is used for permissions

- States
	- Succeed & Fail 
	- Wait
	- Choice - state that allows the state machine to take a different action based on incoming information
	- Parallel - perform multiple sets of things at the same time, e.g. multiples of the choice state
	- Map - performs set of actions that are listed out, once action per item.
	- Task - Single unit of work performed by the state machine; this allows the state machine to do things. (Lambda, Batch, DynamoDB, ECS, SNS, SQS)