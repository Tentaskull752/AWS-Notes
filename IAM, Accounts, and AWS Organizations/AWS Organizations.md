
#### Personal Summary 

  - Allows business to manage multiple AWS accounts in a cost effective way without much overhead. 
  - Standard AWS Account: account not within an organization. You create the organization using this account. This account then becomes the management or master account. 
  - Invites are needed to be given to other standard accounts to join an organization, and they then become member accounts. 
  - At the top of the organization, is the root container. Can contain other containers (Organization Unit (OU)). 
  - Consolidated billing brings all fees and bills from the member accounts to the account that created the organization and possesses the payment method. It's a single monthly bill within the management account comprised of all fees of the accounts within the organization. 
  - You can create new AWS accounts within an organization; NO INVITE PROCESS NEEDED. 
  - IAM Roles can be used to allow IAM users to access other AWS accounts. 
  - Best Practice: Have a single account (management account) that contains all of the identities that are logged into. 

### Questions and Links

