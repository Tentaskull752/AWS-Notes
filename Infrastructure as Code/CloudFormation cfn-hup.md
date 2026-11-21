

- cfn-init loads meta data within the logical resources within a logical stack. A desired-state config tool for EC2 based on meta data. ONLY RUN ONCE
- If cfn-init is updated, it isn't rerun
- cfn-hup helper is a daemon which can be installed to update any changes afterwards the initial bootstrapping
- ....it detects changes in resource metadata
- ...running configurable actions when a change is detected
- cfn-hup, periodically checking the metadata, will then call on cfn-init to implement another configuration when there is an update to the metadata