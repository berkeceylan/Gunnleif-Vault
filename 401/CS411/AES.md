## Advanced Encryption Standard (AES)

### Type:
- [[Symmetric Key Cipher]] and [[Block Cipher]]
### History: 
- Established by the U.S. National Institute of Standards and Technology (NIST) in 2001.
- Serves as the successor to the Data Encryption Standard ([[DES]]).
- First name was Rijndael.
- Detailed AES explanation: [Wiki AES](https://tr.wikipedia.org/wiki/AES)
### Key Length: 
- Supports three key lengths: 128, 192, and 256 bits.
- S-Box used to generate round keys.
- The number of rounds in the transformation process varies:

| Key length(in bits) | Number of rounds |
| ------------------- | ---------------- |
| 128                 | 10               |
| 192                 | 12               |
| 256                 | 14               |
- In every round each bit in the block are treated uniformly
- Since block size is fixed and 128/192/256-bit blocks to encrypt larger data blocks we use [[Modes of Operations]]
### Operation: 
- Not a Feistel Network
	- Therefore it can process whole block which is explains that how it has fewer rounds
- Designed for both hardware and software
- In every round, each bit in the block are treated uniformly
	- After two round each of the 128 output bits depends on each of the 128 input bits
	- Provides high [[Diffusion & Confusion |diffusion]]
- Has three basic steps:
	1. **Key Addition Layer:** XORing the block with the round key
	2. **Byte Substitution Layer:** 
		- Non-linear substitution step where each byte is replaced with another according to a lookup table.
			- 8-by-8 substitution (s-box)
				- $x \mapsto x^{-1} \text{ in } \text{GF}(2^8) = x^8 + x^4 + x^3 + x + 1$
				- Balanced 
				- Highly Non-linear operation (confusion)
			- Has constant mapping (efficiency)
	3. **Diffusion Layer:** 
		- Provides the diffusion of the bits of a block
		- **ShiftRows**: A transposition step where bytes in the block's rows are shifted cyclically.
		- **MixColumns**: A mixing operation which operates on the columns of the data block, combining the four bytes in each column.
- Encryption and Decryption operations are different:
	- **AES Encryption:**
		- ![[AESenc.png]]
	- **AES Decryption:**
		- ![[AESdec.png]]
### Security: 
- No known attacks are better than brute force fır seven or more rounds
- Key length make infeasible the brute force attacks
- Considered as most secured system until now
- Combination of AES with [[CBC]] ensure [[Semantic Security]]
### Current Status:
- Its used most of the security systems and became standardised


