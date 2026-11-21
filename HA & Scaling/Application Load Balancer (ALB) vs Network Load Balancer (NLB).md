

 - Classic Load Balancers don't scale because they don't support SNI, as you can't have multiple SSL certificates per a single Load Balancer.

Application Load Balancer:
 - Layer 7, able to understand both HTTP and HTTPS.
 - Can't understand any other layer 7 protocols such as SMPT, SSH, and Gaming
 - and NO TCP, UDP, TLS Listeners
 - L7 content such as cookies, custom headers, user location and app behavior are understandable. Can take these metrics and create more strategy driven solutions.
 - HTTP and HTTPS (SSL/TLS) always terminated on the ALB - no unbroken SSL
   ...and then a new connection is made to the application from the ALB.
 - All ALBs must have SSL certs if HTTPS is used. 
 - ALB is slower than NLB, there are more levels of the network stack to process. 
 - Health checks evaluate app health @ L7
	 - Rules
		 - Rules direct connects which arrive at the listener
		 - Processed in priority order
		 - Default rule = catchall
		 - Rule Conditions: host-header, http-header, http-request-method, path-pattern, query-string & source-ip
		 - Actions: forward, redirect, fixed-response, authenticate-oidc & authenticate-cognito


Network Load Balancers: 
 - Layer 4 - TCP, TLS, UDP, TCP_UDP
 - No visibility or understanding of HTTP or HTTPS
 - No headers, no cookies, no session stickiness
 - REALLY REALLY REALLY FAST (millions of rps, 25% of ALB latency)
 - SMTP email, SSH, game servers, financial apps, (NOT HTTP/S)
 - Health checks just check ICMP/TMP Handshake, Not app aware
 - Can be given static IP's - used for whitelisting(Allows straight access through a firewall)
 - Forward TCP to instances ... unbroken encryption. NLB and TCP listeners gives unbroken end-to-end encryption where the encrypted section is not terminated by the load balancer. 


ALB vs NLB USE CASES
 - Unbroken encryption - NLB
 - Static IP for whitelist - NLB
 - Fastest performance - NLB (millions rps)
 - Protocols not HTTP or HTTPS - NLB
 - Privatelink - NLB
 - Otherwise - ALB