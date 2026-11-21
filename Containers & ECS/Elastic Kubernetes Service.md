
#### Personal Summary 

  - AWS Managed Kubernetes - open source & cloud agnostic.
  - Can run on AWS, outposts, EKS Anywhere, and EKS Distro
  - Integrates with AWS services...ECR, ELB, IAM, VPC.
  - EKS Cluster = EKS Control Plane & EKS Nodes
  - ectd distributed across multiple AZs
  - Nodes - self-managed, managed groups or Fargate pods
  - Can choose Node type, customizable, windows, GPU, Inferentia, Bottlerocket, Outposts, Local zones
  - Storage Providers: include...EBS, EFS, FSx Lustre, FSx for NetAPP ONTAP
  - EKS Control Plane will run from AWS Managed VPC, the second place will be the customer's personal VPC.
  - Control Plane will interact with the Nodes via their ENI's after the nodes have been injected into the customer VPC.
  - Can also use a Public Control Plane Endpoint, any consumption of services is done Ingress.