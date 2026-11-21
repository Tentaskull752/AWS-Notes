

## Personal Notes

  - What size should the VPC be?
  - Are there any Networks we can't use?
  - Be careful of other IP ranges that other parties use (VPCs, Cloud, On-premises, Partners and Vendors)
  - Try to predict the future and keep possibilities open.
  - VPC Structure: Tiers & Resiliency (Availability) Zones. Networks may be split across this Reliability Zones aka Availability Zones.
  - VPC min. is /28(16IP) and max. is /16(65536 IPs)
  - Personal preference for the 10.x.y.z range
  - AVOID COMMON RANGES- avoid future issues. 10.0 10.1, and 10.1 to 10.10. START AT 10.16.
  - To determine how much IP space a business needs, consider how many regions they are operating in. Then add a few more as a buffer. Have at least 2+ network ranges in each region in each AWS account. 
  - For ex. 3 US regions, 1 Europe regions, and 1 Australia region - assume 4 AWS accounts: TOAL 40 RANGES (ideally).