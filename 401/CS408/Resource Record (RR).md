## Resource Record (RR)
### Definition:
- Records in a [DNS](DNS.md) database
	- Full Example: [DNSDatabaseExample](Attachments/DNSDatabaseExample.png)
- Fields: `DomainName TTL Class Type Value`
	- **Domain Name:** 
		- Series of labels separated by (".")
	- **TLL (Time to live):**  
		- how long to hold the result in local cache (zero means no cache)
	- **Class:** 
		- Usually `IN` for [The Internet](The%20Internet.md)
	- **Types:**
		- **A and AAAA**: 
			- Address Type
			- Value of A -> IPv4 
			- Value of AAAA -> Pv6 
			- Example: `ns1.example.com 86400 I  A 173.11.76` or use AAAA
			- **Glue Records**:
				- Glue records are used to prevent circular dependencies in DNS lookups, by providing the IP addresses needed to contact the authoritative name servers for a domain, directly in the query response to the parent zone.
				- The name servers learns about the next one in the hierarchy using the glue records
			- There might be different IPs for same host
				- For load balancing -> work in round-robin fashion
				- DNS can distribute loads across multiple servers by rotating through a list of IP addresses for a single hostname.
		- **SOA (Start of Authority)**: 
			- Parameters and info about zone
			- Sync with other servers
			- Example:
			`example.com. 3600  IN  SOA  ns1.example.com. hostmaster.example.com. (
				`2020103001 ; Serial`
				`7200       ; Refresh`
				`3600       ; Retry`
				`1209600    ; Expire`
				`86400      ; Minimum TTL`
			`)`
			- Notice!! -> dot replacing the @ symbol
			- `hostmaster@example.com.` ->`hostmaster.example.com.`
		- **MX (Mail Exchange)**: 
			- Directs email to mail servers
			- Value field -> name of the receiving [SMTP](SMTP.md) agent for the Domain_Name
			- Example: `example.com.   3600   IN   MX  mailserver.example.com.`
			- Supporting load balancing through multiple records.
				- Multiple MX RRs: 
					- DNS Server sends out full list list of MX RRs but in different order in every query.
		- **CNAME (Canonical Name)**: 
			- Used to create aliases 
			- Value -> canonical host name for the alias
			- Example: `www.example.com.   3600   IN   CNAME   example.com.`
		- **NS (Name Server)**: 
			- Specifies the name servers for the domain
			- Value -> name of the server
			- Example: `example.com.   3600   IN   NS   ns1.example.com.`
			- Aiding in delegation and distributed management.
				- there might be several DNS Servers for each domain for fault tolerance
		- **PTR (Pointer)**: 
			- Used for reverse DNS lookups
			- Linking an IP address to a canonical hostname
			- Useful when you know the IP address and want to know the corresponding host name
			- Value -> hostname
			- Example: `24.192.140.193.in-addr.arpa.   3600   IN   PTR   example.com.`
				- Searched IP: 193.140.192.24 
				- numbers are given in reverse order
		- **HINFO (Host Information)** and **TXT (Text)**: 
			- Provide additional information about a host or miscellaneous text.
			- Textual data
	- **Value (Rdata = Resource Data):** different for each RR type


