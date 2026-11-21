

 - Synchronous Invocation:
	 - Client sends a request, invoking Lambda, and the answer is returned, either in the form of data or a failure. 
	 - Errors or retries have to be retried within the client.
	 - Can also be done indirectly with API Gateway, which proxies the request to the lambda function, and funnels the answer back to the client.

 - Asynchronous Invocation:
	 - E.G We put data into an S3 bucket, and this data is automatically sent to the Lambda function, which then stores it in Dynamo DB. 
	 - This action is done without S3 waiting for a response or the job to finish. 
	 - If processing of the event fails, Lambda will retry between 0 and 2 times (configurable). Lambda handles the retry logic.
	 - Idempotent reprocessing is a retry mentality that would result in the same end-state or the desired end-state. Don't set the lambda function to add or subtract (e.g. trying to get $10 to $20), just give it the desired result and let it keep trying.
	 - If the auto-retries don't work, the function can send the task to Dead Letter Queues.
	 - Can also send to Destinations (SQS, SNS, Lambda & Eventbridge), where successful or failed events can be sent.


  - Invocation through Event Source Mapping
	  - Typically used on streams or queues which don't support event generation to invoke lambda (kinesis, DynamoDB streams, SQS)
	  - Event Source Mapping polls queues or streams to look for new data. In the form of batches, these are broken up as required and sent to a Lambda function as event batches (can contain hundreds of events in a single batch).
	  - Permissions from the lambda execution role are used by the event source mapping to interact with the event source and capture those data event batches.
	  - Event Source Mapping can send off failed data event batches to SQS Queues or SNS topics. 


 - A version of a lambda function is the code + the configuration of the lambda function.
 - The version is immutable - it never changes once published, and has it's own Amazon Resource Name
 - $Latest points at the latest version
- Aliases (DEV, STAGE, PROD) point at a version (can)


 - An Execution Context is the environment a lambda function runs in. A Cold Start is a full creation and configuration including function code. "The data package has to be downloaded, an execution context is being configured and created, and any perquisites are being downloaded and installed."
 - Warm Start: Lambda uses the same execution context. Doesn't need to download environment or the execution package. Lambda receives the event and immediately starts executing. 1-2 milliseconds.
 - If used infrequently, contexts will be removed. 
 - Can inform AWS in advance and execution contexts can be created before hand. 
 - "If a lambda function used the same environment context, it would have access to the same media as of the previous lambda function".
 - Assume execution context's are stateless, assume nothing will be carried over. 
 - "ANYTHING OUTSIDE OF THE LAMBDA FUNCTION HANDLER, WILL ALLOW THIS ACCESS FOR OTHER LAMBDA FUNCTION INVOCATIONS."