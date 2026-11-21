

 - Avoid v1, using v2 is preferred
 - Classic Load Balancer (CLB) - v1 - can load http and https and lower layered protocol. Not really layer 7, lacks features, and 1 SSL certificate per CLB. Allot more expensive than the other version. 
 - Application Load Balancer (ALB) - v2 - HTTP/S/WebSocket
 - Network Load Balancer (NLB) - v2 - TCP, TLS & UDP. NOT HTTP or HTTPS
 - V2 = faster, cheaper, support target groups and rules. 