### Definition:
- One of the [[Classical Ciphers]]
- Also known as Shift Cipher
- Each letter in the plaintext is shifted a certain number of places down or up
- One to one mapping exist
### Type:
- [[Symmetric Key Cipher]]  and [[Substitution Cipher]]
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
