
- designed to  check on EC2s, the OS's they run on, and any vulnerabilities and deviations against best practice.
- Can check containers as well.
- Length....15  mins, 1 hour, 8.5 hours or 1 day
- Provides a report of findings ordered by priority
- Network assessment (agentless)
- Network & Host Assessment (requires an agent)

- Rules packages determine what is checked and returns findings
- Network Reachability (no agent required)
- ....Agent can provide additional OS visibility
- Check reachability end to end: EC2, ALB, DX, ELB, ENI, IGW, ACLs, RTs, SGs, Subnets, VPCs, VGWs, & Veer Peering

- Common vulnerabilities and exposures (CVE)
- Center for Internet Security (CIS) Benchmarks
- Security best practices for Amazon Inspector (disabling route login over ssh, using only modern version numbers for ssh, password complexity checks, and permissions on certain folders)