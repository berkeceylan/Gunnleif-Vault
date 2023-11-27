### Definition:
- One of the [Classical Ciphers](Classical%20Ciphers.md)
- Use of letter-shifting based on a keyword
- When the letters of the ciphertext are grouped, a one-to-one mapping exist
	- Since every group encrypted with Caesar cipher
### Type:
- [Symmetric Key Cipher](Symmetric%20Key%20Cipher.md) and polyalphabetic [Substitution Cipher](Substitution%20Cipher.md).
### Key:
- Utilizes a keyword or phrase, which determines the shift for each letter in the plaintext.
### Operation:
- Uses different [Caesar Cipher](Caesar%20Cipher.md)s for successive letters based on the keyword. 
- The keyword is repeated to match the length of the plaintext.
### Security:
- **Enhanced Security**: 
	- More resistant to cryptanalysis than mono-alphabetic substitution ciphers due to its polyalphabetic nature.
- **Resistance to Brute Force**: 
	- Traditional brute force methods are less effective
	- Since it use multiple Caesar shifts
- **Vulnerabilities**:
	- **Kasiski Examination**: 
		- A technique that can break the Vigenere Cipher 
		- by examining the distances between repeating sequences of letters in the ciphertext.
	  - **Frequency Analysis**: 
		  - More sophisticated frequency analysis methods can be effective
		  - analyzing longer ciphertexts
	  - **Cryptanalytic Attacks**: 
		  - Known plaintext, chosen plaintext, ciphertext only attack methods work 
