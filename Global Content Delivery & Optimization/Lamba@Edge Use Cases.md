
## Personal Summary

- Feature of CloudFront that allows the running of lightweight Lambda at Edge Locations
- Adjusts data between the Viewer & Origin
- Currently supports Node.js and Python
- Run in the AWS Public Space (NOT VPC)
- Layers are NOT SUPPORTED
- Different Limits vs Normal Lambda functions

- Use Cases:
	- A/B Testing - Viewer Request Function. Receives viewer request and changes URL based on what object is wanted
	- Migration Between S3 Origins - Origin Request. Can use a weighted value to determine the amount of traffic that heads to the new origin
	- Different Objects Based on Device - Origin Request. Will display images based on the specs (Dots per inch of screen for ex). Higher specs, gets a bigger sized and quality object
	- Content by Country - Origin Request