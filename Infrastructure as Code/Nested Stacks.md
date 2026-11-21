
- ****THERE IS A LIMIT OF 500  RESOURCES PER STACK! CAN"T EASILY REUSE RESOURCES!! CAN"T EASILY REFERENCE OTHER STACKS!!!! RESOURCES IN A SINGLE STACK SHARE A LIFECYCLE  ***

- Nested Stacks:
	- Start with the Root/Parent Stack (the one created first either manually or through automation)
	- Have to give the nested stack URL code to the CloudFormation site to create the child-stack within it's instructions

- *** Whole templates can be reused in other stacks with URL Templates
- ***Use when the stacks form one part of the solution - lifecycle linked

- Use Nested Stacks to 
	- overcome the 500 Resource Limit of one stack
	- Modular templates...reuse
	- Make the installation process easier...
	- ....nested stacks created by the root stakc
	- USE ONLY WHEN EVERYTHING IS LIFECYCLE LINKED
	- Want one resource to last longer than another? NOPE
	- Need to use the same actual VPC? Use cross-references
	- Make changes to one part of the application only? Have individual and non nested stacks and use cross-references


- Child Templates must be within S3; you cannot reference local files. You must upload child templates to: Amazon S3
- Parameter: a variable defined in a CloudFormation template whose value is supplied when the stack is created or updated. 