## Message Digest 5 (MD5)

### Definition:
- It is a one of the common examples of [Cryptographic Hash Functions](Cryptographic%20Hash%20Functions.md)
- Based on the [Merkle-Damgard Construction](Merkle-Damgard%20Construction.md) 
- Detailed information about [MD5](https://www.geeksforgeeks.org/what-is-the-md5-algorithm/)

### Properties:
- **Fixed Output Size**: 
	- MD5 produces a 128-bit hash value, regardless of the input size.
- **Fast Computation**: 
	- It is designed to be quick and efficient in generating the hash for any size of data.
- **Deterministic**: 
	- The same input will always yield the same output hash.
- **Pre-image Resistance**: 
	- It is computationally hard to reverse the hash
	- To find an input that corresponds to a particular hash.
- **Avalanche Effect**: 
	- Small changes to the input result in a significantly different hash.
### Operation:
- Operations based on [Merkle-Damgard Construction](Merkle-Damgard%20Construction.md)
	- It follow same steps with these values
		- Blocks size  = 512 bits
		- Hash value = 128 bits
	- IV = four 32-bit words
### Current Status:
- In past used extensively but now its not considered as secure:
	- **Brute force attack:**
		- Since its hash value is 128 bits $2^{64}$  is not considered secure any more because of [Birthday Attack](Birthday%20Attack.md)
