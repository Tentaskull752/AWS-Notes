

 - Allow configuration of custom actions during autoscaling process (instance creation and termination).
 - Instances pause during these two states' flows. THEY WAIT...
	 - until a timeout (continue or abandon). The state changes when timeout (3600s default) expires OR...
	 - or you resume the ASG process CompleteLifecycleAction

 - Scale-out Steps:
	 - Pending
	 - Pending: Wait
		 - here you can index or load data
	 - Pending: Proceed
	 - InService
 - Scale-in Steps:
	 - Terminating
	 - Terminating: Wait
		 - here you can backup data or logs
	 - Terminating: Proceed
	 - Terminated