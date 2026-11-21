
#### Personal Summary 

   - A policy that can be attached to an entire organization through the root contain or attached to one or more organization units; can also be attached to individual AWS accounts. 
   - It trickles down if attached to the root and entire container to individual accounts and branched organization units. But if attached to these individual items, it won't affect the higher up accounts or other items at all.
   - SCPs are account permissions boundaries. They LIMIT what the account (including account root user) can do. BUT you can NEVER restrict the account root user, BUT if you restrict the account, then you THEN restrict the account root user. 
   - SCPs don't grant permission, they just set boundaries. 
   - When you enable SCPs, AWS grants a policy named FULL AWS ACCESS as a default. Now SCPs have no effect. For ex. "DenyS3" deactivates S3 for an entire account. DENY, ALLOW, DENY
   - An ALLOW LIST deactivates the Full AWS Access, and then a new policy explicitly allows access to services such as S3 for example. 

![[Pasted image 20250921185730.png]]
### Questions and Links

