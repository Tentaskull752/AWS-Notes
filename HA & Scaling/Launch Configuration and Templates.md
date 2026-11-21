

 - Both allow the configuration of an EC2 instance in advance.
 - Defines AMI, instance type, storage, storage & key pair.
 - Networking and Security Groups
 - Userdata & IAM Role
 - Both are NOT editable - defined once. LT has versions.
 - LT provide new features - T2/T3 unlimited, placement groups, capacity reservations, elastic graphics. 
- Launch Configuration
	- Used as a part of Auto Scaling Groups
	- Used for config. of the ec2's used by auto scaling groups. 
	- No editing, have to create a new one from scratch
- Launch Template
	- Can be used by Auto Scaling Group, but also can be launched directly from the dashboard. 
	- Can be used to save time when provisioning EC2 instances from console UI/CLI 