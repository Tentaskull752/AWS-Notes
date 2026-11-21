
## Personal Summary

-  Encrypted & Authenticated tunnel
- Over DX (Low Latency & consistent latency)
- Uses a Public VIF + VGW/TGW public endpoints
- VPN is Transit Agnostic (DX/Public Internet)
- VPN is end-to-end CGW <-> TGW/CGW - MACsec is single hop based
- VPN has Wider vendor support
- VPN has more CRYPTOGRAPHIC overhead vs MACsec...limits speeds
- VPN can be used while DX is being provisioned and/or as a DX backup
- Public VIF directly connects the Customer gateway to the public zone endpoints created by the VPN/VPC. This gives direct access and low latency compared to all the hops and high latency of going through the aws system on the public internet all around the world.