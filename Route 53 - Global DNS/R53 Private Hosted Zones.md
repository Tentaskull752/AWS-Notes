
## Personal Summary

 - Not public, only associated and accessible with VPCs within AWS. 
 - Split-view (overlapping public & private) for PUBLIC and INTERNAL use with the same zone name
 - In order for a vpc to access dns, there has to be an application within the vpc trying to query the dns record, it goes through the VPC +2 address, and is associated with dns, it then has access. 
 - A public hosted zone can be setup with the same name as the private hosted zone and it can access certain resource records from the private zone. It does the usual following the tree of ISP Resolver, to the root servers, to the .ORG records, to the name servers that host animals4life.org.
 - only available within one or more vpc's