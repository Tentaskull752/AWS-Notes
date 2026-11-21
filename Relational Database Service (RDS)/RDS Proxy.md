

## Personal Summary

 - WHY?
	 - Opening and closing connections to DB's consumes resources
	 - Takes time, creating latency
	 - With serverless, every lambda opens and closes
	 - Managing failure of DB instances is difficult
	 - ...doing it within your application adds risk

 - DB Proxies changes the architecture, instead of an application connecting to the DB/instances, they connect to the proxy, which then routes it to the DB. It is pool of connections. 
 - Auto scaling & highly available by default
 - Only accessible from a VPC
 - Accessed via Proxy Endpoint
 - Can enforce SSL/TLS
 - The proxy runs throughout all AZ's of the DB Cluster, and possesses a Long Term Connection Pool. 
 - Proxy connections are quick to establish and place no load on the instances. 
 - Can use the same long term connection in the future (sort of like a cache)
 - Multiplexing - a smaller number of proxy connections can be used for a larger number of application requests
 - In the case of failure, the application connect to the proxy, and proxy will wait until the new primary instance is determined.

- Uses:
	- Too many connection errors
	- DB instances using T2/T3 (smaller/burst) instances
	- AWS Lambda...time saved/connection reuse & IAM AUTH
	- Long Running connections (SAAS apps) - low latency
	- Where resilience to database failure is a priority
	- RDS Proxy can reduce time for failover by over 60%
	- ...and make it transparent to the application. Abstracts failure away from your applications


 