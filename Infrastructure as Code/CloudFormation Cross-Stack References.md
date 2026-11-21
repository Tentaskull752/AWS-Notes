
- The problem here is the isolation and self-containment feature of CloudFormation
- Say we want a VPC within a stack to be usable by other regions and accounts
- Outputs are normally not visible from other stacks due to isolation of CloudFormation
- (root stack of) Nested stacks can reference them...
- Outputs can be EXPORTED...making them visible from other stacks
- Exports must have a unique name in the region, this exported value goes into an export list along with a name (ex. SHARED VPCID)
- Fn::ImportValue can be used instead of Ref

- Cross-reference allows reuse of stack resources and nested stacks allow you to reuse Templates