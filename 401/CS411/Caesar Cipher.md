### Definition:
- One of the [Classical Ciphers](Classical%20Ciphers.md)
- Also known as Shift Cipher
- Each letter in the plaintext is shifted a certain number of places down or up
- One to one mapping exist
### Type:
- [Symmetric Key Cipher](Symmetric%20Key%20Cipher.md)  and [Substitution Cipher](Substitution%20Cipher.md)
### Key: 
- A single integer (the shift value)
- The total number of valid distinct keys (shift values) = 25
### Operation: 
- Each letter in the plaintext is shifted a fixed number of places down or up the alphabet.
- Encryption: 
	- $y = Ek(x) = x + k \mod 26$
- Decryption: 
	- $x = Dk(y) = y- k \mod 26$
### Security: 
- Easily broken using frequency analysis or brute force
	- Ciphertext only attack method
	- Also can be broken with
		- Known Plaintext
		- Chosen Plaintext
		- Chosen Ciphertext
