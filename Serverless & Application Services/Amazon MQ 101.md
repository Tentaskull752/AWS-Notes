

 - SNS and SQS are AWS services utilizing APIs
 - SNS provides TOPICS and SQS provides QUEUES
 - BOTH are Public Services, highly scalable, AWS integrated

 - Amazon MQ:
	 - Open-source message broker
	 - NOT A PUBLIC SERVICE, NEED A PRIVATE CONNECTION NETWORK BETWEEN ON-PREMISES AND AWS
	 - Based on Managed Apache ActiveMQ
	 - JMS API, protocols such as AMQP, MQTT, OpenWire and STOMP
	 - Provides both QUEUES and TOPICS
	 - One-to-One or One-to-Many
	 - Single Instance (test, dev, cheap) or HA Pair (Active/Standby)
	 - No AWS native integration....delivers activeMQ product which you manage
	 - A Direct Connection or Site-to-Site VPN can be used to connect the On-premises and AWS realms. 

 - SNS or SQS for most new implementations (default)
 - SNS or SQS if AWS integration is required (logging, permissions, encryption, service integration)
 - Amazon MQ if you need to migrate from an existing system with little to no application change
 - Amazon MQ if APIs such as JMS or protocols such as AMQP, MQTT, OpenWire, and STOMP are needed
 - REMEBER YOU NEED PRIVATE NETWORKING FOR AMAZON MQ