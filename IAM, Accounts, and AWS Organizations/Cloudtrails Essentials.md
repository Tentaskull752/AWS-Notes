
#### Personal Summary 

   
 "If you stop an instance, it's logged. If you delete an account, it's logged."
 - Logs API calls/activities as a CloudTrail Event. An action performed by a user, role, or service; recording for 90 days at no cost BY DEFAULT. 
 - Trail logs events FOR THE REGION THAT IT'S IN. Or it can be set to ALL REGIONS(records all region trails, but it looks as one on the outside). 
 - When a trail is set to ALL Regions, GLOBAL services such as IAM, STS, and Cloudfront can send their activities to a trail at Northern Virginia US-East-1 for example. These are known as Global Service Events. These Global Service Events will need to be ENABLED in it's settings for this. 
 - Management and Data events are all captured by the trail attached to that specific region(s). 
- When creating a trail, you can reach beyond the 90 days of recording limit. You can store the trail data in S3 buckets as JSON format files and you will be charged for the amount of space you take up only. 
- An organizational trail from the management account of the org. can be created to store the info from all the accounts in the org. 
- Management event: terminating a bucket, starting an instance, logging in.
- Data event: need to be allowed explicitly and incur a cost. 
- CLOUDTRAIL IS NOT REALTIME, TAKES WITHIN 50 MINUTES OF THE OCCURENCE OF AN EVENT.
