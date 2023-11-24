## Secure Hash Algorithm 2 (SHA-2)

### Definition:
- Proposed by NIST in 2002 as standard
- It is an example of [[Cryptographic Hash Functions]]
- Based on the [[Merkle-Damgard Construction]] 
- Detailed information about [SHA2](https://en.wikipedia.org/wiki/SHA-2)
- SHA-2 includes several hash functions with different digest sizes: 
	- SHA-224
	- SHA-256
	- SHA-384
	- SHA-512
### Properties:
- **Fixed Output Sizes**: 
	- SHA-2 hash functions produce hashes of different lengths: 224, 256, 384, or 512 bits.
- **Fast Computation**: 
	- It is designed to be quick and efficient in generating the hash for any size of data.
- **Deterministic**: 
	- The same input will always yield the same output hash.
- **Pre-image Resistance**: 
	- It is computationally hard to reverse the hash
	- To find an input that corresponds to a particular hash.
- **Avalanche Effect**: 
	- Small changes to the input result in a significantly different hash.
- **Collision Resistant:**
	- Until this day we can not find any weak or strong collusion.
- Compatible security with  [[AES]]

### Operation:
- Operations based on [[Merkle-Damgard Construction]]
	- It follow same steps with these values
		- Blocks size  = 512 or 1024 bits
		- Hash value = 224, 256, 384, or 512 bits.

|                     | SHA-224    | SHA-256    | SHA-384     | SHA-512     |
| ------------------- | ---------- | ---------- | ----------- | ----------- |
| Message Digest Size | 224        | 256        | 384         | 512         |
| Message Size        | $< 2^{64}$ | $< 2^{64}$ | $< 2^{128}$ | $< 2^{128}$ |
| Block Size          | 512        | 512        | 1024        | 1024        |
| Word Size (IV)       | 32 (32x7)   | 32 (32x8)  | 64 (64x6)  | 64 (64x8)          |
| Number of Steps     | 64         | 64         | 80          | 80          |

- Number of steps: The number of rounds or iterations each block of the message goes through during the hashing process.
### Current Status:
- **Security**: SHA-2 is currently considered secure and is widely used for various applications, including SSL/TLS certificates, digital signatures, and other cryptographic security protocols.

