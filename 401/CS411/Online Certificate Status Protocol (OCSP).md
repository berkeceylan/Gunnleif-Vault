### Definition: 
-  A method of revocation in [Certificates](401/CS411/Certificates.md)
- [The Internet](401/CS408/The%20Internet.md) protocol used for obtaining the revocation status of an [X.509 Certificates](401/CS411/X.509%20Certificates.md)
- No need to download whole [Certificate Revocation List (CRL)](Certificate%20Revocation%20List%20(CRL).md)
	- Prevent inefficient list downloading issues in [Public Key Infrastructure (PKI)](401/CS411/Public%20Key%20Infrastructure%20(PKI).md)
### Usage: 
- Client sends a request to an OCSP server with the specific certificate in question
	- maintained by the CA or a trusted third party
- Server responds with the certificate's status 
	- valid, revoked, or unknown
### Advantages: 
- Provides a more efficient and timely way to check a certificate's status
- Reduce the overhead associated with CRLs.