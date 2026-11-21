

 - 3 types:
	 - EC2 - stopping, stopped, terminated, shutting down or impaired (not 2/2 status) = UNHEALTHY
	 - ELB - Healthy = Running & passing ELB health check
	 - If using application load balancer, checks can be more aware.
	 - Custom - instances marked healthy & unhealthy by an external system
	 - Heath check grace period (default 300s) - delay before starting checks
		 - ....allows system launch, bootstrapping and application start