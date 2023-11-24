## Secure Hash Algorithm (SHA-1)

### Definition:
- Proposed by NIST in 1995 as standard
- It is an example of [[Cryptographic Hash Functions]]
- Based on the [[Merkle-Damgard Construction]] 
- Detailed information about [SHA1](https://en.wikipedia.org/wiki/SHA-1)
### Properties:
- **Fixed Output Size**: 
	- Produces a 160-bit hash value, regardless of the input size.
- **Fast Computation**: 
	- It is designed to be quick and efficient in generating the hash for any size of data.
- **Deterministic**: 
	- The same input will always yield the same output hash.
- **Pre-image Resistance**: 
	- It is computationally hard to reverse the hash
	- To find an input that corresponds to a particular hash.
- **Avalanche Effect**: 
	- Small changes to the input result in a significantly different hash.
- Similar to [[DES]], the chaining values are processed in 20 rounds
### Operation:
- Operations based on [[Merkle-Damgard Construction]]
	- It follow same steps with these values
		- Blocks size  = 512 bits
		- Hash value = 160 bits
	- Word size : 32
	- Number of steps : 80
	- IV = five 32-bit words
### Current Status:
- In past used extensively but now its not considered as secure:
	- **Brute force attack:**
		- Since its hash value is 160 bits $2^{80}$  is not considered secure any more because of [[Birthday Attack]]
		- 2005 Wing, Yin and Yu --> find collusion requiring fewer than $2^{69}$
		- 2006 Wang, Yao and Yao --> find collusion requiring fewer than $2^{63}$
		- 2017 Google --> [SHAttered attack](https://en.wikipedia.org/wiki/Shatter_attack)
			- They generated two different PDF files with same hash value $\approx 2^{63.1}$
