
## Personal Summary

  - Used when optimizing for performance & user-experience. 
  - Each record can have a specified region, and Latency-Based Routing allows one record with the same name for each AWS region. 
  - AWS maintains a database of latency between the users general location and the regions tagged in records.
  - It sends back the record/IP address with the lowest latency based on the querier's location.