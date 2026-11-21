

 - Function-as-a-Service (FaaS) - short running & focused
 - Lambda Function - a piece of code that Lambda runs
 - Functions use a runtime (e.g. Python 3.8)
 - Functions are loaded and run in a runtime environment. (That runtime is baked into that Lambda function, one and done)
 - The environment has a direct memory (indirect CPU) allocation
 - You are billed for the duration that a function runs. 
 - A KEY PART OF SERVERLESS ARCHITECTURE

- A package of data is sent to the function, the runtime is written in the function, the package is then downloaded and worked on by the function via the runtime. 
- Supported runtimes: Python, Ruby, Java, Go, C#
- Docker - traditional container-ized computing. Use an image to create a docker container to use in compute environments. 
- Each runtime within the function requires it's own specific runtime environment with it's own specific components. 

 - Memory can be from 128 Mb to 10240 MB (with 1 Mb steps), you directly control the memory allocated for lambda functions, whereas vCPU is allocated indirectly. Assume it's blank every time a lambda function is invoked.
- Lambda can run up to 15 MINUTES, known as FUNCTION TIMEOUT.

 - Common Uses:
	 - Serverless Applications: S3, API Gateway, Lambda
	 - File Processing: S3, S3 Events, Lambda
	 - Database Triggers: DynamoDB, Streams, Lambda 
	 - Serverless CRON: EventBridge/CWEvent + Lambda
	 - Realtime Stream Data Processing: Kinesis + Lambda