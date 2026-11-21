
## Personal Summary

  - In a hosted zone for animals4life.org for example, there can be multiple records pointing at at the same application/associated IP address.
  - If the primary resource record (www) passes the health check, the querier is sent to the application. 
  - BUT if the primary resource records fails, then the second resource record is queried and sends the querier to a second site containing the wanted information (an S3 bucket for example.)
  - "A common architecture is to use failover for a 'out of band' failure / maintenance page for a service (e.g EC2 / S3)"