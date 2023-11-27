### Definition:
- A notion to describe the security of an encryption scheme
	- Goldwasser and Micali in 1982
- Ciphertext reveals no information about the plaintext
- No (or negligible) information should be extracted from the ciphertext
### Properties:
- **No Information Leakage**:
	- Attacker should not  obtain any information about the plaintext from the ciphertext.   
- **Probabilistic Encryption**: 
	- Encrypting the same plaintext multiple times results in different ciphertexts
	- Example: Protection form SPA attack in [RSA](RSA.md) created with [OAEP](OAEP.md) 
- **Security Against Chosen-Plaintext Attacks**:
	- Attacker has the ability to choose plaintexts and receive their corresponding ciphertexts, but still should not be able to derive any meaningful information about any other plaintexts.
 - **Practical Implication**:
	 - Even attacker try exhaustive search it should not break the cipher text