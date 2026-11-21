
## Personal Notes

  - Lifecycle Configuration is a set of rules, and these rules are sets of actions that can be set upon buckets or groups of objects within a bucket. 
  - Transition actions: actions that move objects between S3 Storage classes if lets say for ex. a rule says "any objects not accessed for 90 days goes into infrequent instant access."
  - Expiration actions: deletion of the object if inactivity reaches a set point. 
  - Configurations can help save costs as buckets increase in numbers and activity.
  - Beware of transferring smaller objects from standard to Standard-IA, Intelligent-tiering, and One Zone due to the minimum size requirement for the object or a fee will be incurred. 
  - An object must remain in S3 Standard for 30 days before being transferred into Intelligent or One Zone. 
  - You cannot create a single rule that transfers an object from Standard to the Infrequent tiers before the 30 days min., and you cannot do the same for Infrequent tiers to the Glacier tiers. Two rules, each implemented after the two 30 days min. periods can be put into place. 