

 - Public AWS Service - network connectivity with Public Endpoint, can be accessed from the public internet with the right AWS permissions
 - Coordinates the sending and delivery of messages
 - Messages are <= 256KB payloads
 - SNS Topics are the base entity of SNS - permissions and configuration
 - A publisher sends messages to a TOPIC
 - TOPICS have Subscribers which receive messages
 - e.g. HTTP(s), Email, SQS, Mobile Push, SMS Messages & Lambda
 - Filter - filter on a subscriber that limits messages based on the service's functionality
 - Fanout - a topic with multiple SQS Queues as subscribers

- Delivery Status - (HTTP, Lambda, SQS)
- Delivery Retries - Reliable Delivery
- HA and Scalable (Region)
- Server Side Encryption (SSE)
- Cross-Account via TOPIC Policy