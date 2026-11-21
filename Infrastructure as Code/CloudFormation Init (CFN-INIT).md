

- CFN-INIT is a simple configuration management system
- Configuration directives stored in template
- AWS::CloudFormation::Init part of logical resource
- Procedural - HOW (User Data)
- ....vs Desired State WHAT (cfn-init)

Stack roles allow an IAM role to be passed into the stack via PassRole

A stack uses this role, rather than the identity interacting with the stack to create, update and delete AWS resources.

It allows role separation and is a powerful security feature.

Config Keys - containers of configure directives 
Config Set - set of config keys to use and in what order 