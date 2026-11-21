
#### Personal Summary 

 EC2 Mode
  - Handles scheduling and orchestration, cluster management, and placement of engines.
  - ECS Cluster is placed within a VPC in your AWS account. When you creating cluster, you specify wanted number of instance clusters. Auto-Scaling Group will control the number of instances automatically, a form of horizontal scaling. 
  - From a container registry, container images are placed onto their own container instances within the cluster. 
  - SELF-MANAGED, pricing, availability, number of container hosts, security, connection with a registry. 

Fargate Mode
 - NO SERVICE TO MANAGE. 
 - Use the same task and service definitions, but these are allocated to the shared Fargate platform (like physical hardware that hosts the data and applications of multiple customers).
 - Each task is injected into the vpc and is given an Elastic Network Interface. Uses these Network Interface to interact with these tasks and services. 
 - Tasks and services can be given public IPv4 addresses if they are set that way at initial setup. 
 - No visibility of host cost or available space, no host management or provisioning. Only pay for what you consume. 


- IF YOU USE CONTAINERS, USE ECS
- LARGE WORKLOAD - PRICE CONCIOUS - EC2 MODE 
- LARGE WORKLOAD - OVERHEAD CONSCIOUS - FARGATE
- SMALL/BURST WORKLOADS - FARGATE
- BATCH/PERIODIC WORKLOADS - FARGATE 
