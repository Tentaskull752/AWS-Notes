

 - Bridging:
	 - (default of app. load balancer): listener is configured for HTTPS.  Connection is terminated on the ELB & needs a cert. for the domain name.
	 - ELB initiates a new SSL connection to backend instances. Instances need SSL certs and the compute required for cryptographic operations.
	 - Instances will need matching SSL certificates as the domain.
	 - Load balancer sees uncrypted HTTP, but SSL cert need to be stored on Load Balancer (downside), instances need it as well.
- Pass-through:
	- Network Load Balancer sends user straight to the backend instance unencrypted.
	- Listener is configured for TCP. No encryption or decryption at NLB. 
	- Each instance needs to have appropriate SSL cert installed.
	- No certificate exposure to AWS, self-managed and secured. 
- Offload:
- Listener is configured for HTTPS. Connections terminated and then backend connections use HTTP
- ELB to instance connections using HTTP, no cert. or cryptographic requirements.

Stickiness:
- with no stickiness connections are distributed across all in-service backend instances. Unless application handles user state this could cause user logoffs shopping cart losses.
- Stickiness generates a cookie which locks the device into a single backend instance for a set duration (can be 1 sec of 7 days).
- Stickiness/session can be hosted externally., make the architecture stateless.