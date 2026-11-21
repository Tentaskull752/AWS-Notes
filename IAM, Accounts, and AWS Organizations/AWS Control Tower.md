 - Allows for the quick and easy setup of multi-account environments. 
 - Orchestrates other AWS services to this end
 - Organizations, IAM, Cloud-formation, Config and more
 - Landing Zone - multi-account environment
 - SSO/ID Federation, Centralized Logging and Auditing 
 - Guard Rails - Detect/Mandate rules/standards across all accounts
 - Account Factory - Automates and standardizes new account creation. 
 
 - An account creates a Control Tower Landing Zone and becomes the Manager account. Initially consists of Control Tower, SSO, and AWS Organizations. 
 - Federated ID and internal ID are used to log people in through IAM/SSO
 - Then two Organization Units are created: "Security/Foundational" and "Sandbox/Custom". 
 - Audit account and Log Archive Account are created within the Security/Foundation OU; 
 - Log Archive Account for users who need to access login information for all accounts within the landing zone. This includes read-only access to AWS Config and Cloudtrail logs for ex.
 - Audit account is for users who need access to audit info made available by Control Tower. Can also be a location for any 3rd party tools for anything to audit the account(s). SNS for notifications to changes to governance and security policies  and Cloudwatch for monitoring landing zone-wide metrics.
 - Account Factory: modifying, adding, and deleting accounts based on personal needs. Within the Custom OU, it will create AWS accounts in fully automated method. Configuration is handled on two templates based on account and network properties. 
 - Control Tower uses Cloudformation for most of this account configuration, and uses Config to set up Guardrails that detect drifts away from governance standards and even prevent them. 
 - The home region, the one you deploy the landing zone into is always available. 
 - Sandbox OU is used for testing/less rigid security. 
 - You can create other OU's and accounts.
 - IAM/SSO, multiple accounts, ID Federation (use existing identity stores to access all these AWS accounts)
 - Monitoring and Notifications: Cloudwatch and SNS
 - Guards are rules for multi-account governances; Mandatory, strongly recommended or elective.
 - Guardrails: 
	 - Preventive - stops you doing things
		 - enforced or not enable
		 - allow or deny regions or disallow bucket policy changes
	 - Detective - compliance checks (AWS Config Rules)
		 - clear, in violation or not enables
		 - detect cloudtrail enabled or EC2 Public IPv4
	 - Accounts can be closed or repurposed
	 - Can be fully integrated with a business SDLC

	Automated Account Provisioning
		 - cloud admins or end users (with appropriate permissions)
		 - Guardrails auto-added
		 - Account admin given to a named user(IAM Identity Center)
#### Personal Summary 

   
