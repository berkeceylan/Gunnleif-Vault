Used in [DNS Operation](DNS%20Operation.md) 
## Iterative vs. Recursive Queries

### Recursive Queries:
- If one name server does not know the queried host
- It acts like a [DNS](DNS.md) client and asks to next name server in the zone hierarchy.
- Then sends the result back recursively
### Iterative Queries:
- If the name server does not know the host
- Then returns the address of the next server in the zone hierarchy
- But does not ask that server.

**nslookup**: A command-line tool for querying the DNS to obtain domain name or IP address mapping.
**Active and Passive Mode**: DNS supports both active querying and passive responses for efficient data retrieval.
**Remark1**: The name servers learns about the next one in the hierarchy using the glue records.
**Remark**2: Queries and responses are sent over [UDP](UDP.md) 
