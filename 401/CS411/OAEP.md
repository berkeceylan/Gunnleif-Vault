## Optimal Asymmetric Encryption Padding (OAEP)
### Definition:
- OAEP is a padding scheme used in the encryption process
- Mostly used with [[RSA]]
- It add randomness into the encryption process of RSA
	- Provide protection form side channel attack
	- Ensure [[Semantic Security]] in RSA
- Ensures that the same plaintext will yield different ciphertexts even if encrypted multiple times with the same key
- Uses two rounds of [[Feistel Network]] and [[Cryptographic Hash Functions]] to create desired uniform randomization
### Operation:
- **Encryption:**
	![[OAEPencryption.png]]
- **Decryption:**
	![[OAEPdecryption.png]]