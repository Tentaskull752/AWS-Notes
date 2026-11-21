
- Record configuration changes in resources overtime; this change is called a Config item
- Great for auditing changes, compliance with standards
- Does not prevent changes from happening, not a permissions or protection product
- Regional service ... supports cross-region and account aggregation
- Changes can generate SNS notifications and near-realtime events via EventBridge & Lambda

- Config rules: AWS or customer managed. Evaluate resources against defined standards, they are either compliant or non-compliant. 
- Config rules use Lambda to check whether resources are good against the standards. 