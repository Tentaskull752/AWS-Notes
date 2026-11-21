

## Personal Notes


 VPC Router: highly available router located in every VPC. Has a Network interface; in every subnet 'network+1' address.
  - Simply routes traffic between subnets
  - Route tables defines what VPC router will do when data leaves a subnet. 
  - If you don't create and assign a personal route table, VPC will default to Main route table, the subnet default. Subnet can only have one route table at one time, but route table can have many subnets at one time.
 - Higher prefix (last number of IP destination) is more specific and therefore has HIGHEST PRIORITY. LOCAL ROUTE ALWAYS TAKE PRIORITIES, EVEN OVER SPECIFICITY RULE. 
 - A route matches a destination IP for that route and directs traffic to that target.


 - Internet Gateway: REGION RESILIENT gateway attached to a VPC. One gateway call cover all AZs in the region that the VPC is using.
 - 1 VPC = 0 or 1 IGW, 1 IGW = or 1 VPC. 
 - Runs from within the AWS Public Zone
 - Gateways traffic between the VPC and the Internet or AWS Public zone (S3, SQS, SNS)
 - Managed- AWS handles performance


 - 1. Create IGW
 - 2. Attach IGW to VPC
 - 3. Create custom RT
 - 4. Associate RT
 - 5. Default routes =>IGW
 - Subnet allocate IPv4

IPv4 ADRESSING:
 - An EC2 during allocation of a public IPv4 address, does not touch the services within the VPC. A record is created that the internet gateway maintains, and links the instance's private ip to its public allocated IPv4. Only private IP is seen in the O.S.


 - BASTION HOST = JUMPBOX
 - It's an Instance in a public subnet
 - Incoming management connections arrive there
 - Then access interval VPC resources
 - Often the only way IN to a VPC.