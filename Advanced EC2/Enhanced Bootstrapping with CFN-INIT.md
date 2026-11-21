
## Personal Summary

 - cfn-init is a helper script - installed on EC2 OS. Is a simple configuration management system.
 - Procedural (UserData) vs Desired State (cfn0init). Desired State is just telling the OS where you want the final state to be configuration wise, and it will do whatever is necessary to get there.
 - Can control packages, groups, users, sources, files, commands and services to achieve wanted state.
 - Provided with directives via Metadata and AWS::CloudFormation::init on a CFN resource. It executes the Metadata "EC2Instance" related instructions, then executes the UserData bit of instructions.
 - UserData part of UserData has variables that will be replaced with actual values once transplanted into cfn-init. For ex. stack ID and region. 
 - CFN-INIT WORKS WITH STACK UPDATES. User Data only executes once, but if something changes, CFN-INIT CAN CHANGE ALONG WITH IT. 


 - EC2 can't detect non-working results made from the User Data. A Creation Policy is something added to a logical resource within Cloudformation. This is used to create a stack, then used to create an instance. It doesn't give an automatic "ok" like EC2, it waits for a signal from the resource, Cloudsignal specifically. If CNF-Signal reports an error, then Cloudsignal is sent an error message. If there is a time out, then the instance is not allowed to complete properly.