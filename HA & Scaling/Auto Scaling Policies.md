

 - ASGs don't need scaling policies - they can have none.
 - Manual - Min, Max & Desired - Testing & Urgent
 - Simple Scaling - an action if an alarm goes into an alarm state (if CPU goes over 40%, delete instance). But it's not very efficient
	 - you're adding and removing the same amount of instances now matter how dramatic the deviation from the desired value is. Could be 40% away from desired, but 2 instances will still be added.
 - Step Scaling - change desired value based on step adjustments that are based on the size of the alarm breach. There are tiers of responses. if 20-30% +1, if 40-60% +2
 - Target Tracking - keeps desired value as priority, and performs actions to keep it there. The farther away from the desired value, the more dramatic the action will be to get back to the desired value.
 - Scaling Based on SQS