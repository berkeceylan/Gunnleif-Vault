### Definition:
- Provide authentication using [Symmetric Key Cipher](Symmetric%20Key%20Cipher.md)(Encryption)
- Key Distribution Center (KDC) -> trusted authority act as a key server
	- Each party shares own master key with KDC  
	- KDC generates session keys used for connections between parties  
	- Master keys are used to distribute these session keys in a secure way
- Protocols:
	- [Needham-Schroeder Protocol](Needham-Schroeder%20Protocol.md)
	- [Kerberos](Kerberos.md)