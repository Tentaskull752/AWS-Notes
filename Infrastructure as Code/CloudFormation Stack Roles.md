

- CFN uses the permissions of the logged in identity to create physical resources
- ...meanings you NEED permissions to create, update, or delete stacks or resources for said stacks
- CFN can assume a role to gain the permissions
- Lets you implement role seperation
- The identity creating the stack...doesn't need resource permissions - only PassRole


Stack roles allow an IAM role to be passed into the stack via PassRole

A stack uses this role, rather than the identity interacting with the stack to create, update and delete AWS resources.

It allows role separation and is a powerful security feature.