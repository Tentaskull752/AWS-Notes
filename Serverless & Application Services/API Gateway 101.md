

 - Create and Manage APIs (Application Programing Interface, allows programs to communicate with each other)
 - Endpoint/entry-point for applications
 - Sits between applications &
 - Highly available, scalable, handles authorization, throttling, caching , CORS, transformations, OpenAPI spec, direct integration with AWS services
 - Public, can connect to services/endpoints in AWS or on-premises
 - HTTP APIs, Rest APIs, and Websocket APIs.
 - Can also use Lambda for computing

 - API Gateway Cache can be used to reduce the number of calls made to backend services/integration and improve client performance
 - Cloudwatch Logs can store and manage full stage request and response logs. Cloudwatch can store metrics for clients and integration services.
 - ![[Pasted image 20251228000423.png]]


 - Authentication:
	 - Cognito - takes the token from 3rd party application authentications and produces temp. AWS credentials. Passes token with asking of entry into API Gateway. 
	 - Lambda Authorizer - natively validates this authorization within the request. Does this itself, or calls upon an ID provider or compute based check of ID

 - Endpoint Types:
	 - Edge-Optimized
		 - Routed to the nearest CloudFront POP
	 - Regional - Clients in the same region
	 - Private - Endpoint accessible only within a VPC via interface endpoint 

- Stages:
	- APIs are deployed to stages, each stage has one deployment. Customers could access the prod. stage, developers and the dev stage. 
	- Versions of lambda can be assigned to each stage. 
	- Canary Deployments - deployments are made to the canary, not the stage. Stages enabled for canary can have a percentage of its traffic sent to the canary. This can be adjusted over time, or the canary is promoted to the new base 'stage'

- Errors (REMEMBER THESE FOR EXAM)
	- 4XX - Client Error - Invalid request on client side
	- 5XX - Server Error - Valid request, backend issue
	- 400 - Bad Request - Generic client-side error, could have many causes
	- 403 - Access Denied 0 - Authorizer denies ..WAF Filtered
	- 429 - API Gateway can throttle - this means you've exceeded this amount
	- 502 - Bad Gateways Exception - bad output returned by lambda
	- 503 - Service Unavailable - backend endpoint offline? Major service issues
	- 504 - Integration Failure/Timeout - 29s limit

 - Caching:
	 - Cache TTL default is 300 seconds, configurable min 0 and max 3600s. 
	 - Can be encrypted
	 - Cache size 500MB to 236 GB
	 - Reduced load & Cost with its use
	 - Calls are only made to backend integrations if request is a cache miss
	 - Cache is defined per stage within API Gateway