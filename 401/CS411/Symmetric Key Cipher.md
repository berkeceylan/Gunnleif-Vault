### Definition:
- [Cryptographic](Cryptography.md) algorithm where the same key is used for both encryption and decryption of data. 
- The key must be known and kept secret by both the sender and the receiver.
### Properties: 
- **Shared Key**: 
	- The same key is used for encrypting and decrypting the data.
	- Both encryption and decryption keys are known to and shared by the communicating parties
	- The keys are often related or identical. 
- **Key Secrecy**: 
	- The security of the communication depends on the secrecy of the shared key.
	- Knowledge of one key can lead to the derivation of the other.
- **Efficiency**: 
	- Symmetric key algorithms are fast and more efficient than [asymmetric key algorithms](Asymmetric%20Key%20Cipher)
	- Used to encrypting large volumes of data
- **Key Distribution Challenge**: 
	- A major challenge: 
		- secure distribution of the key to both parties without it being intercepted
	- Public Key Cryptography (PKC) solves this issue (to detailed information go to PKC note)
### Examples:
- **[DES](DES.md) (Data Encryption Standard)**:
	- **Key Size**: 56-bit
	- **Vulnerability**: brute force attacks due to its smaller key size.
- **[3DES](3DES.md) (Triple DES)**: 
	- An enhancement of DES that applies the DES algorithm three times to each data block.
- **[AES](AES.md) (Advanced Encryption Standard)**:
	- **Key Sizes**: 128-bit, 192-bit, or 256-bit 
	- Know as one of the most secure system
-  **[Caesar Cipher](Caesar%20Cipher.md)**
-  **[Affine Cipher](Affine%20Cipher.md)**
- **[Vigenere Cipher](Vigenere%20Cipher.md)**