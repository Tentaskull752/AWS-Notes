
## Personal Summary

-  A Network Transit Hub to connect VPCs to on premise networks
- Significantly reduces network complexity
- Single network object - HA and Scalable
- Attachments to other network types
- VPC, site-site VPN & Direct Connect Gateway attachments

- Instead of needing a mesh system of VPCs with the VPN, and then each VPC needing a connection with each CGW, USE A TRANSIT GATEWAY so the 4 VPCs only need to attach to the Transit Gateway, and the CGWs only need a single connection to the Transit Gateway
- You can PEER Transit Gateways to gain cross-region same/cross-account to create a global network within AWS. 
- TGW come with a default route table which routes information between the attachments (the 4 VPCs that it's connected to)

- Supports transitive routing
- Can be used to create Global Networks via Peering
- Can share TGW between different AWS accounts via AWS RAM (allows sharing of products or services, or their components)
- Peer with different regions... same or cross account
- TGW IS LESS COMPLEX THAN TRADITIONAL VPC MESHED NETWORK