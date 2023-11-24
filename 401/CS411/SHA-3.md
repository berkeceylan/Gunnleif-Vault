## Secure Hash Algorithm 3 (SHA-3)

### Definition:
- Winner of NIST's competition in 2012
- It is an example of [[Cryptographic Hash Functions]]
- Based on the [Keccak Algorithm](https://www.geeksforgeeks.org/difference-between-sha-256-and-keccak-256/)
- Detailed information about [SHA3](https://en.wikipedia.org/wiki/SHA-3)
### Properties:
- **Flexible Output Size**: 
	- Can produce hashes of various lengths (like SHA-224, SHA-256, SHA-384, and SHA-512)
	- Capable of arbitrary output lengths
- **Sponge Construction**: 
	- Produce an output bit stream of any desired length
		- via SHAKE128/256 extendable output functions (XOFs)
		- generate as many bits from its sponge as requested
	- [Sponge Function](https://en.wikipedia.org/wiki/Sponge_function)
	- Different from the Merkle-Damgård construction
- **High Security**: 
	- Designed to be resistant to cryptanalytic attacks known to affect other SHA functions.
- **Efficiency**: 
	- Efficient in both hardware and software implementations.
### Operation:
- The operation of SHA3 is based on Keccak Algorithm which is uses the Sponge Construction
	- Due to this construction's flexibility different hash lengths (like SHA3-224, SHA3-256, SHA3-384, SHA3-512) 
	- Output bit stream size is not fixed we can get desired bit stream size via Sponge

|                     | SHA3-224   | SHA3-256   | SHA3-384   | SHA3-512  |
| ------------------- | ---------- | ---------- | ---------- | --------- |
| Message Digest Size | 224        | 256        | 384        | 512       |
| Message Size        | no max     | no max     | no max     | no max    |
| Block Size          | 1152       | 1088       | 832        | 576       |
| Word Size (IV)      | 64 (64x18) | 64 (64x17) | 64 (64x13) | 64 (64x6) |
| Number of Steps     | 24         | 24         | 24         | 24        |
### Current Status:
- **Security**: SHA-3 is considered highly secure and not susceptible to the same vulnerabilities as SHA-1 and SHA-2.
