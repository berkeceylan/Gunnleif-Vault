### Definition:
- Method of encryption where elements of the plaintext are systematically replaced with other elements.
### Properties:
- **Single or Polyalphabetic**:
	- **Single Alphabetic**:
		- Each letter is replaced by another letter, maintaining a one-to-one mapping 
		- Example: Caesar Cipher
	- **Polyalphabetic**: 
		- Uses multiple substitution alphabets, changing the substitution rule throughout the encryption process 
		- Example: Vigenere Cipher
- **Fixed System of Replacement**: 
	- The system of substitution is predetermined and must be known by both sender and receiver.
### Examples:
- **[Caesar Cipher](Caesar%20Cipher.md)**: 
	- Shifts all letters in the plaintext by a fixed number down or up the alphabet.
- **[Vigenere Cipher](Vigenere%20Cipher.md)**: 
	 - Uses a keyword to determine the shift for each letter in the plaintext.
 - **[Affine Cipher](Affine%20Cipher.md)**
### Security:
- **Frequency Analysis**: 
	- Simple substitution ciphers are vulnerable to frequency analysis
	- Attacker studies the frequency of elements in the ciphertext to deduce the substitution method.