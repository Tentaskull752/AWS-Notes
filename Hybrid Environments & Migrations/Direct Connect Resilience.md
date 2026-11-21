
## Personal Summary

-  When you gain access to an AWS DX Port at the Direct Connect Location, YOU NEED TO get access to equipment to gain access to the customer premises via customer or provider DX Router (in the form of a port.)
- This is known as a single cross-connect.

- Single Points of Failure - DX Location, DX Router, Cross Connect, Customer DX Router, Extension, Customer Premises & Customer Router

- If there are multiple DX Routers, you can have multiple Cross Connects (multiple customer DX Routers and multiple Customer Premises Routers)

 - A better architecture: 2 DX Locations, 1 cross connect in each DX Location, 2 Customer Premises and one connection in each to the Customer DX Router
 - MAXIMUM RESILIENCE: 2 DX Locations, 2 DX Routers in each DX Location  2 customer DX Routers and 2 cross connections in each DX Location, 2 Customer Premises and two router in each premises, each with a connection to the Customer DX Router (so 4 connections TOTAL)