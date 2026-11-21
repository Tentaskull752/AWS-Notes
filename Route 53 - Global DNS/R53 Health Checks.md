
## Personal Summary

  - Health checks are separate entities than records, they are configured externally, and are used by records.
  - Health checkers are located globally. 
  - Checks are done ever 30 seconds, or 10 seconds at an additional cost.
  - TCP, HTTP/HTTPS, HTTP/HTTPS WITH STRING MATCHING
  - Healthy or Unhealthy, if over 18% report that the application is healthy, then the overall report is deemed as healthy.
  - Endpoint, CloudWatch Alarm, Checks of Checks (Calculated)