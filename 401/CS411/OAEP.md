s## Optimal Asymmetric Encryption Padding (OAEP)
### Definition:
- OAEP is a padding scheme used in the encryption process
- Mostly used with [RSA](RSA.md)
- It add randomness into the encryption process of RSA
	- Provide protection form side channel attack
	- Ensure [Semantic Security](Semantic%20Security.md) in RSA
- Ensures that the same plaintext will yield different ciphertexts even if encrypted multiple times with the same key
- Uses two rounds of [Feistel Network](Feistel%20Network.md) and [Cryptographic Hash Functions](Cryptographic%20Hash%20Functions.md) to create desired uniform randomization
### Operation:
- **Encryption:**
	![](OAEPencryption.png)
- **Decryption:**
	![](OAEPdecryption.png)