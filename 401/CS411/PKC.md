## Public Key Cryptography (PKC) 

### Definition
- Solves the problem of secret key distribution and management in [Cryptography](Cryptography.md)
- Proposed by Diffie/Hellman in 1976
- Its a  [Asymmetric Key Cipher](Asymmetric%20Key%20Cipher)
- **Examples:**
    - [RSA](RSA.md)
    - DL
    - Elliptic curve cryptosystems 
    - IBE -\> Id is the public key
    - Lattice-based cryptosystems 
### Properties:
- Each user has a pair of keys which are generated together under a scheme 
	- Private key -> known only to the owner
	- Public key -> known to anyone in the systems with assurance 
	- Public and private key system based on [Ring](Ring.md)
 - Encryption and decryption methods are public 
	 - Encryption
		 - Sender encrypts the message by the public key of the receiver 
	- Decryption
		- Only the receiver can decrypt the message by her/his private key 
- Based on mathematical problem -> Computational infeasibility 
- Much slower than [Symmetric Key Cipher](Symmetric%20Key%20Cipher.md)
### Applications:
- **Encryption/Decryption**: 
	- Used for encrypting short messages due to computational intensity
		- not used the encryption of large data since it is slow
- **Digital Signatures**: 
	- Message digest is encrypted with the sender’s private key
	- Anyone with the public key can verify the message's authenticity
- **Key Exchange**: 
	- Provide secure key exchange in cryptographic protocols.

-----------------------Below part need further investigation------------------------------------
### Connection with Other Cryptographic Concepts
- **Hash Functions**: Digital signatures in PKC often use cryptographic hash functions like SHA-2 or SHA-3 to create message digests before encryption.
- **Block Ciphers and AEAD**: PKC is complementary to symmetric key cryptography (like AES). In many protocols, PKC is used for secure key exchange, while symmetric key cryptography handles the bulk of data encryption due to efficiency.
- **Non-repudiation**: PKC, especially RSA, provides non-repudiation in digital signatures, ensuring a message can be verifiably attributed to the sender.