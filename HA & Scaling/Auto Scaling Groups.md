

 - ASG provide automatic scaling and self-healing for EC2. 
 - Make use of configuration within Launch Templates or Configurations. 
 - Minimum, Desired and Maximum Size (e.x 1:2:4)
 - Keep running instances at the Desired Capacity by provisioning or terminating instances. Can update size values and EC2 will do the necessary work.
 - Scaling Policies automatically change the desired number between the min and max values.
 -  Subnet within a VPC are selected to run ASG. There is a desired to keep an even number of instances across all subnets designated for the ASG. 
 - Scaling Policies:
	 - Manual scaling - manually adjust the desired capacoty
	 - Scheduling scaling - time based adjustment - e.g. Sales
	 - Dynamic Scaling:
		 - Simple - "CPU above 50% +1", "CPU below 50% -1"
		 - Stepped Scaling - Bigger +/- based on difference, "CPU above 80%"
		 - Target tracking - Desired Aggregate CPU = 40% ...ASG handle it. Will provision or delete instances to stay at the amount of performance
	 - Cooldown Period - sets how long for ASG to wait after an instance provision or deletion to see metric changes before performing another action. 
	 - Self-healing: health check says that an instance is ill, ASG deletes and replaces this instance with a new one. 

 - Scaling Processes:
	 - Launch and Terminate - SUSPEND and RESUME
	 - AddToLoadBalancer - add to LB on launch
	 - AlarmNotifications - accept notification from CW
	 - AZRebalance - Balances instances evenly across all of the AZs
	 - HealthCheck - instance health checks on/off
	 - ReplaceUnhealthy - Terminate unhealthy instances and replace
	 - ScheduledActions - scheduled on/off
	 - Standby - use this for instances 'InService vs Standby'

 - ASG are free
 - Only the resources created are billed
 - Use cool downs to avoid rapid scaling
 - Think about more, smaller instances - granularity
- Use with ALB's for elasticity - abstraction
- ASG controls WHEN and Where(what subnet or AZ), LT defines WHAT