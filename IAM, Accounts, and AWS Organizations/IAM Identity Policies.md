
#### Personal Summary 


JSON Statements contain the:
 - "Sid": the name of the statement
 - "Effect": what you determine to happen to this account, are they ALLOWED or DENIED?
 - "Action": what are you gaining access to or being denied from? For ex. 'S3:*' to get into S3 buckets to manipulate objects. 
 - "Resource": sort of a link to the resource itself.

EXPLICIT DENIES ALWAYS WINS OVER EXPLICIT ALLOWS

DENY, ALLOW, DEFAULT DENY. IF IT'S NOT GRANTED ACCESS, THEN YOU HAVE NO ACCESS

Inline Policy: Go through the project itself, create JSON statements giving anyone who is given access, the ability to act upon the resources in full access. Then create this policy in each account for whomever wants to get into this project. USED AS EXCEPTIONAL ACCESS RIGHTS

Managed Policy: Create the Json with statements and it's a single document, then send this out to anyone whom you want to get into the project. 
### Questions and Links

