### Definition:
- Type of a [cryptographic](Cryptography.md) encryption algorithm
- Encrypts data in fixed-size blocks
### Type
* [Symmetric Key Cipher](Symmetric%20Key%20Cipher.md) that encrypts data one block at a time.
* It can be demonstrated as simple [Substitution Cipher](Substitution%20Cipher.md) with large character size.
* **Examples:**
	* [Hill Cipher](Hill%20Cipher.md)
	*  [DES](DES.md) (Data Encryption Standard)
	- [AES](AES.md) (Advanced Encryption Standard)
### Operation:
- Family of functions which maps n-bit plaintext blocks to n-bit cipher blocks
	- n is called the block-length
		- Block size increase -> security increase
	-  [one-to-one mapping](one-to-one%20mapping)
	- Function parameterized by a k-bit key K
### Key:
- Typically a binary string of a fixed length 
- **Example:**
	- [DES](DES.md) key length = 56 bits (not secure)
	- [AES](AES.md) key length = 128, 192 and 256 bits
  - Since block size is fixed to encrypt larger data blocks we use [Modes of Operations](Modes%20of%20Operations.md)
### Security:
- #### Diffusion:
	- Achieved through operations that spread the influence of individual plaintext bits across many cipher text bits. 
	- **Example:**
		- In [AES](AES.md), the ShiftRows and MixColumns steps contribute to diffusion.
- #### Confusion:
	- Achieved through substitution operations, which replace input bits in a non-linear and unpredictable manner. 
		- **Example:**
			- In [AES](AES.md), the SubBytes step uses an S-box to achieve this.