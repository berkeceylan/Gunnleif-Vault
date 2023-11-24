 [[Cryptography |Cryptographic]] attack methods used in cryptanalysis
### Ciphertext Only Attack
- **Access**: Attacker only have the ciphertext
- **Goal**: Derive the plaintext or the key used to encrypt the message
- **Challenges**:
	- Limited information makes this attack the most difficult.
	- Often involves trial-and-error methods like brute force or statistical analysis.
### Known Plaintext Attack
- **Access**: Attacker have both the plaintext and its corresponding ciphertext
- **Goal**: Determine the encryption key 
- **Approach**:
	- Analyze the relationship between the plaintext and the ciphertext.
	- Often used to find vulnerabilities in the encryption algorithm.
### Chosen Plaintext Attack
- **Access**: Attacker can choose plaintexts and obtain their corresponding ciphertexts
- **Goal**: Derive the encryption key or gain insights about the encryption algorithm
- **Approach**:
	- Selectively choose plaintexts to reveal maximum information about the encryption method.
	- Common in scenarios where attackers can manipulate inputs in a system.
### Chosen Ciphertext Attack
- **Access**: Attacker can choose arbitrary ciphertexts and obtain their corresponding plaintexts.
- **Goal**: Discover the decryption key or properties of the decryption process
- **Approach**:
	- Focuses on manipulating ciphertexts to extract information about the decryption key or method.
	- Often applicable in scenarios with interactive decryption systems, such as some digital signature schemes.