

 - Built to run and scale 3rd party appliances in a scalable way, such as: Firewalls, Intrusion Detection, and Prevention Systems.
 - Inbound and Outbound traffic (transparent inspection and protection)
 - GWLB Endpoints - traffic enters/leaves via these endpoints
 - GWLB balances packets across multiple backend instances/appliances.
- GENEVE is a tunneling protocol, a tunnel from the GWLB endpoints to the backend instances, traffic and metadata are channeled through this. 
- Traffic is sent to the endpoint first, via the routing table. This traffic goes to the GLWB, goes through the GENEVE Encapsulation (tunnel). Original packets remain unaltered encapsulated through to appliances & back. A response is sent back via GENEVE to the GWLB, to the endpoint, and finally to the traffic destination/app server. 