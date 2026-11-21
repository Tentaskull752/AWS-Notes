

- Logical Resources in a template - WHAT you want
- CFN uses to Create, Update, and Delete physical resources
- CloudFormation doesn't support EVERYTHING: CUSTOM RESOURCES IS THE ANSWER
- Custom Resources let CFN integrate with anything it doesn't yet, or doesn't natively support
- Passes data to something, gets data back from something. When CR is created, updated, or deleted, a message is sent to that destination
- 