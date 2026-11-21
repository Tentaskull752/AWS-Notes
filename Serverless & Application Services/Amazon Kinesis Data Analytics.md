

 - Service providing real time processing of data
 - Using Structure Query Language (SQL)
 - Ingests from Kinesis Data Streams or Firehose
 - Destinations: Firehose(S3, Reshift, ElasticSearch & Splunk), AWS Lambda, Kinesis Data Streams


- There are four realms: Source Stream, Reference data, Kinetics Analytics App., and Destination Stream.
- The Source Stream (Kinesis Stream and Firehose) send in In-application input stream to SQL operating within the Kinesis Analytics App.
- Application Code processes Input and produces Output
- Static data from the Reference Data(S3 bucket) to enrich the streaming input
- SQL creates In-application output stream, and these are sent to the applications within the Destination Stream (Kinesis Stream and Firehose)
- Errors created from Processing by the SQL, is sent to In-application error stream
- Using Kinesis Analytics, you can use complex SQL queries to manipulate input data into whatever form of output data you want

 - Use-Cases:
	 - Streaming data needing real-time SQL processing
	 - Time-series analytics....elections or e-sports
	 - Real-time dashboards - leaderboards for games
	 - Ream-time metrics - Security & Response teams 