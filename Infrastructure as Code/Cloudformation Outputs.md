
- Output section is optional, these values can be declared in this section, and visible as outputs when using CLI, in the console UI, and accessible from Parent stack when using nesting.
- Can be exported, allowing cross-stack references
- Description: something visible from the CLI and Console UI & Passed back to parent stack when nested stacks are used
- Value: determines exactly what you want to be exposed by the parent stack when creation is completed. 
- Value is created via !Join Intrinsic function connecting literal string "https://" and logical resource attribute DNS name