
- Allows deployment of CFN stacks across many accounts & regions
- StackSets are containers in an admin account...
- ....they contain stack instances...which reference stacks; container for an individual stack
- Stack instances & stacks are in 'target accounts & regions'
- Each stack = 1 region in 1 account
- Security = self-managed IAM Roles or service-managed Permissions ***

- Concurrent Accounts: How many individual AWS accounts can be used at the same time. Set at 2, only two accounts can be deployed into at once
- Failure Tolerance: amount  of individual employments that  can fail before  the stack set  itself is viewed as failed
- Retain Stacks: remove stack instances from a stack set, and by default, it will delete any of the stacks within the target accounts; a setting can be changed to retain those TA stacks
- Scenario: Enable AWS Config across multiple accounts
- Scenario: AWS Config Rules - MFA, EIPS, EBS Encryption
- Scenario: Create IAM Roles for Cross-account access