

 - It isn't one single thing
 - You aim to manage few, if any servers - low overhead
 - Applications are a collection of small & specialized functions
 - ...functions run in stateless & ephemeral environments - duration billing
 - Event-driven...consumption only when being used 
 - FaaS is used where possible for compute functionality
 - Managed services are used where possible (S3, dynamodb & 3rd party identifiers such as google or facebook)
 - Elastic Transcoder Service: a service in AWS that can take in media, transcode it, and generate media of different sizes from the original video file. 
 - A Transcode bucket and DynamoDB receive these newly altered videos. 
 - There can be a lambda that consists as a "My Media" that moves through the Transcode bucket and DynamoDB to determine which videos are the client's and creates URL's and sends to the client. 