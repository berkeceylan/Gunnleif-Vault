### Definition:
- **Problem:**
	- Distribution and the security of the keys is a big problem
	- Even the algorithm is secure we may unable to distribute or protect keys over a network
### Key Agreement:
- **Idea of Protocol:**
	- Protocols whereby a secret key is established by exchanging information between two or more parties
	- Each party derives the secret key from the exchanged information
- **Protocols:**
	- [PKC](PKC.md) -> not suitable multiple(n>2) user
	- [Conference Keying](Conference%20Keying.md)  -> suitable for multiple(n>2) user
	- [Diffie-Hellman Key Exchange](Diffie-Hellman%20Key%20Exchange.md)
		- Do not provide authentication -> [Man-in-the-Middle Attack](Man-in-the-Middle%20Attack.md)
	- [Station-to-Station Protocol](Station-to-Station%20Protocol.md)
		- Authenticated version of DH
		- Has [Forward Secrecy](Forward%20Secrecy.md)
### Key Distribution:
- **Problem:** (with key pre-distribution protocols)
	- Keys are predetermined and not easily changed
	- Keys must be changed after certain time
- **Solution:** 
	- Transport protocols
	- A class of key establishment protocols
	- Two approaches:
		- One party to decide on a key and transmit it to other
		- A trusted authority will act as a key server
			- [Key Distribution Center (KDC)](Key%20Distribution%20Center%20(KDC).md)
- **Protocols:**
	- [Needham-Schroeder Protocol](Needham-Schroeder%20Protocol.md)
	- [Kerberos](Kerberos.md)
### Key Management:
- Use of Public Key Cryptography ([PKC](PKC.md)) to distribute secret keys
	- public/private key as a master key
- [Public Key Infrastructure (PKI)](Public%20Key%20Infrastructure%20(PKI).md)
- How can I make sure about the legitimacy of a public key?
	- Public Announcement
		- Broadcast your public key to the public via forums, mailing lists, from personal website, whatsapp, social media, etc.
		- Major weakness is anyone can easily pretend as yourself 
	- Publicly available databases/directories
		- There exists a directory/database for name, public key pairs
		- Write controlled by a trusted administrator  
		- If administered thoroughly, this method is good.
		- However, a proper administration is difficult. 
		- Secure mechanisms for registration, update and delete is required.
	- [Certificates](Certificates.md)

