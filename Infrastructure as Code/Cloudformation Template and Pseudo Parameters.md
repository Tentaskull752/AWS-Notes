
- Template Parameters accept input - console/CLI/API
- ...when a stack is created or updated (size of instance or type of environment)
- Parameter values can be referenced within Logical Resources
- ...influencing physical resources and/or configuration
- Can be configured with Defaults, AllowedValues, Min and Max length & AllowedPatterns, NoEcho & Type

- Pseudo-Parameters: populated by AWS, can match things such as stack name, stack ID, or Account ID. THEY FETCH CRUCIAL INFORMATION TO MINIMIZE PHYSICAL INPUT
- Minimize number of parameters that require explicit inputs, so use defaults, and getting values from AWS rather than the person working through AWS
- "You can use pseudo parameters instead of hard-coded values to make your templates more portable and easier to reuse across different AWS accounts and Regions."