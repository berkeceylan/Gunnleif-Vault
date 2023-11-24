### Definition:
- Type of a [[Cryptography |cryptographic]] encryption algorithm
- Encrypts data in fixed-size blocks
### Type
* [[Symmetric Key Cipher]] that encrypts data one block at a time.
* It can be demonstrated as simple [[Substitution Cipher]] with large character size.
* **Examples:**
	- [[AES]] (Advanced Encryption Standard)
	- [[DES]] (Data Encryption Standard)
### Operation:
- Family of functions which maps n-bit plaintext blocks to n-bit cipher blocks
	- n is called the block-length
	-  [[one-to-one mapping]]
	- Function parameterized by a k-bit key K
### Key:
- Typically a binary string of a fixed length 
- **Example:**
	- [[Hill Cipher]] not considered as secure
	- [[DES]] key length = 56 bits
	- [[AES]] key length = 128, 192 and 256 bits
  - Since block size is fixed to encrypt larger data blocks we use [[Modes of Operations]]
### Security:
- #### Diffusion:
	- Achieved through operations that spread the influence of individual plaintext bits across many cipher text bits. 
	- **Example:**
		- In [[AES]], the ShiftRows and MixColumns steps contribute to diffusion.
- #### Confusion:
	- Achieved through substitution operations, which replace input bits in a non-linear and unpredictable manner. 
		- **Example:**
			- In [[AES]], the SubBytes step uses an S-box to achieve this.