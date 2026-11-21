
- Has two versions: Standard (free) & Advanced (has a cost)
- Protects against DDOS attacks:
	- Network Volumetric Attacks (L3) - saturate capacity with requests
	- Network Protocol Attacks (L4) - TCP SYN Flood, send in requests with no intention of closing them to prevent new and genuine connections
	- Application Layer Attacks (L7) - e.g web request floods

- Standard:
	- Free
	- Protection at the perimiter
	- ...region/VPC or at the AWS Edge
	- Common Network (L3) or Transport (L4) layer attacks
	- Best protection using R53, CloudFront, AWS Global Accelorator

- Advanced:
	- Costs $3,000 per month per organization, part of a 1-year commitment. Charge for Data Out as well
	- Protects CF, R53, Global Accelerator, Anything associated with EIPs (i.e EC2), ALBs, CLBs, NLBs
	- Not automatic - must be EXPLICITLY enabled in Shield Advanced or AWS Firewall Manager Shield Advanced policy
	- Cost Protection for unmitigated attacks. Something that Advanced should be able to cover, but misses, so you avoid those costs
	- Proactive Engagement & AWS Shield Response Team (SRT) - automatic contact about your performance being impacted by an attack. Contact details needed in advance and enabling of product
	- Integration with AWS Firewall, includes basic WAF fees for web ACLs, rules, and web requests
	- Application Level 7 DDOS protection using WAF
	- Real time visibility of DDOS events and attacks
	- Health-based detection - application specific health checks, used by proactive engagement team
	- Protection groups: protection products grouped together; decreases admin overhead.