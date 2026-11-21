
-  Cloudformation tries to do things efficiently....by  doing  things in parallel (create, update & delete at the same   time)
- ...tries to determine a dependency order (VPC > Subnets > EC2s)
- ...references or functions create these
- DependsOn lets you explicitly define these
- If Resources B and C depend on A
- .....both wait for A to complete before starting

- Can't Ref a resource until it is fully completed, gateway attachment with a VPC can't be completed until the VPC and other necessary resources are created first. 

- ON TEST: Creating an Elastic IP requires an IGW attached to a VPC in order to work, BUT there is not dependency in the  template. There is an order of resource creation
- The Elastic IP will only be created when the IGW attachment is established; and the Elastic IP will be deleted BEFORE the IGW is deleted. 