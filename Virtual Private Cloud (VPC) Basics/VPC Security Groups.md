

## Personal Notes


  - Security Groups are stateful; detect response traffic automatically 
  - Allowed (In or Out) request = allowed response
  - NO EXPLICIT DENY ... only ALLOW or Implicit DENY
  - can't block specific bad actors. Typically use NACL's where they are used to add explicit denies. 
  - Supports IP/CIDR and logical resource references; including other SGs and ITSELF
  - SGs are attached to specific ENIs (Primary Network Interface); when you attach an SG to an Instance, the instance is actually attached to this ENI. 
  - Logical References: when one resource is communicating with another within the VPC (two EC2s for ex). When one sends a request, the second could use the first's IP address or the range of the subnet. OR it could reference the SG of the first subnet. It then references anything that have THAT specific SG attached to it.
  - Logical referencing scales... any new Instances which use the webSG are allowed to communicate with any Instances using the APP SG.
  - Self-Referencing: A SG can reference itself, and anything that has this SG can receive anything that have this SG attached. IP changes of are automatically handled. 