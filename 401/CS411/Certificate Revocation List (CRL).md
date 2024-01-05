### Definition:
- A method of revocation in [Certificates](401/CS411/Certificates.md)
- A CRL is a list of [Certificates](401/CS411/Certificates.md) that have been revoked before their scheduled expiration date by the Certificate Authority (CA) that issued them
### Usage:
- Clients download the CRL to check if a particular certificate is listed
- If a certificate is on the list, it is considered revoked and should not be trusted
### Drawbacks:
- CRLs can grow very large over time and can be cumbersome to download and process, especially in environments with limited bandwidth or resources