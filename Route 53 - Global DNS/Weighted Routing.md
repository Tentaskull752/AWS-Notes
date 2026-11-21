
## Personal Summary

  - Each record within a hosted zone (for ex 3) gets it's own weight, and the rate of it being returned to the querier is Record weight / Total weight
  - If record 1's weight is 40, 2's is 40, and 3's is 20. Then the name/IP sent to the querier will be 1 and 2 40% of the time, and 3 20% of the time.
  - If the weight is set to zero, then that name/IP will not be sent at all. IF ALL RECORDS ARE 0, THEN ALL ARE CONSIDERED
  - If a chose record is Unhealthy, the process of selection is repeated until a healthy record is chosen.