
## Personal Summary

- EC2 Bootstrapping is done using User Data, accessed via the meta-data IP.
- http://169.254,169.254/latest/user-data
- Anything in User Data is executed by instance OS
- USER DATA ONLY EXECUTED ONCE AT LAUNCH.
- EC2 doesn't understand it, OS needs to understand the User Data. Boot volume passes data into instance and an OS process runs this as root user.
- User Data to the EC2 is just a block of data, no importance.
- It's not secure, don't use it for passwords or long credentials. 
- User data is limited to 16 KB in size
- User data can be modified if instance is shut down, and data is modified, and instance is turned on again.
- USER DATA IS ONLY EXECUTED ONCE

- AMI to a functioning instance usually takes just a few minutes.
- Post Launch Time: extra (manual or automatic) configuration after an instance is launched. A few minutes or a few hours. 
- Bootstrapping automates installations after an instance launch. It cuts down that wait time of Post Launch Time. 
- AMI Baking: doing the configurations upfront and creating an AMI image with these customizations. 