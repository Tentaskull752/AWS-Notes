
#### Personal Summary 

 - Managed container-based user service.
 - Runs in two modes, EC2 and Fargate. 
 - Container Definition: gives information to ECS of where the container is. Port location is given as well. DEFINES IMAGE & PORTS
 - Task: a self-contained application, could have one or many defined containers. The application as a whole, stores whatever container definitions to make up that application. 
 - Task Definition: stores security/permissions and resources used by a task, memory and cpu. Store networking, stores TASK ROLE (IAM role the task can assume to interact with AWS resources.) TASK ROLES ARE THE BEST PRACTICE TO GIVE CONTAINERS PERMISSIONS TO PRODUCTS AND SERVICES
 - When you create a task definition, you create a container definition (USUALLY 1) along with it. 
 - Service Definition: defines a service (how we want a task for ECS to scale). 
 - Service tells how to go along with scaling, averting and recovering from failure, how a task functions. Tells how many copies you want to run. 
 - A task is a instance within the task definition, the latter of which is unit of power. 