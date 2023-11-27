### Definition:
- The Hill Cipher is a polygraphic substitution block cipher.
- One of the Block Ciphers
### Type:
- [Substitution Cipher](Substitution%20Cipher.md), [Symmetric Key Cipher](Symmetric%20Key%20Cipher.md) and [Block Cipher](Block%20Cipher.md)
### Key:
- A matrix 
- Needs to be invertible modulo the size of the alphabet
### Operation:
- Treats a block of plaintext letters as a vector, then multiplies the vector with the key matrix to produce the ciphertext
### Plaintext/Ciphertext Block Size:
- Determined by the size of the key matrix
- For instance, a 2x2 matrix will work on blocks of 2 letters at a time
### Security:
- Vulnerable to known-plaintext attacks
- Not considered secure by modern standards
- **Diffusion:**
	- Achieved through the matrix multiplication operation
	-  A small change in the plaintext or the matrix can result in a significant change in the ciphertext.
- **Confusion:**
	- Limited in the traditional Hill cipher
	- The relationship between the plaintext and ciphertext is linear, which limits the cipher's resistance to cryptanalysis