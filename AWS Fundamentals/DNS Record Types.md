
### Personal Summary

Nameserver: Root sends a request to the .com servers that house (for ex.) Amazon.com. This then sends a request to their nameservers that houses the wanted records within the Amazon.com zone.

A and AAAA: Host is sending a request to an IP; A www creates a v4 IP address and AAAA www creates a v6 IP address. 

CNAME: Host to Host requests: CNAMEs are functions that are attached to the A server record. The CNAME only points to other names, not IP addresses. And if the A server changes, the CNAMEs need not be updated. 

MX:  Start with google.com zone, there's a record named "A mail" pointing to an IP address. Also in the zone is two MX records; they have a priority and a value. A mail is the host, know this bc it doesn't have a dot on the far right. If you add a dot on the right, it's a fully qualified domain name. It goes from Root, to google.com, to hi@google.com, which then sends an MX query to the google.com zone. The priority of each record is considered, the lower the value, the higher priority granted to the record. A mail is the highest, then MX 10 mail, then MX 20 mail.other.domain. The email server gets the result back, and uses an SMTP (finds mail server for a domain) to connect to the mail server and deliver the mail. 

TXT: want to add a domain to an email system, that system can ask for proof of domain ownership. It'll say "make it have a txt saying 'cats are the best', it'll then send a query to the zone, and it'll be ok'd. 

TTL - Time To Live: Client queries DNS on resolver server, it goes to DNS Root, that points to .com Registry authorities servers, then points to the name of the amazon.com records, the resolver then goes to the amazon.com zone and gets IP address and connect to the server. TTL value can be set to a number(3600 for ex.) and this answer is cached for that hour. If another client queries and goes through the same route of requests, they will get a non-authoritative answer almost immediately due to the answer being cached. Authoritative and non authoritative a practically the same thing.
  
### Revealing Questions







### Insightful Links