### Defintion:
- A mathematical algorithm that maps data of arbitrary size to a bit string of a fixed size (a hash). 
- It is a one-way function, meaning it cannot be reversed, making it suitable for cryptography.
	- Inverting a hash function should be computably infeasible
- Produces a fixed-length output = hash (hash code, message digest or hash value)
	- $h = H(M)$
- Used widely in authentication and digital signature creation
- **Examples:**
	- [[MD5]]
	- [[SHA-1]]
	- [[SHA-2]]
	- [[SHA-3]]
### Properties:
- **Deterministic**: 
	- The same input will always produce the same output.
- **One-way Property**:
	- **Fast Computation**: 
		- Efficient for both hardware and software.
		- $H(x)$ is easy to compute for any given $x$
	- **Pre-image Resistance**: 
		- Reversing the hash computationally infeasible 
		- For any $h$ value it is computationally infeasible to find $x$
- **Message Representativeness:**
	- A change to any bit (or bits) in the message results in a big change to the hash value.
	- **Avalanche Effect**
- **Collision Resistance**:
	- **Weak Collision Resistance:**
		- For a given hash output and a known input, it should be hard to find another input that results in the same hash.
		- For any given message $x$, it is computationally infeasible to find $x \neq y$ such that $H(x) = H(y)$
		- Difficulty of finding collision = $2^n$ trials
			- To be secure it should be at least $2^{100}$
	- **Strong Collision Resistance:**
		- For any given hash function, it should be computationally infeasible to find any two distinct inputs that produce the same hash output.
		- It is computationally infeasible to find ==any== pair $(x,y)$ with $x \neq y$ such that $H(x) = H(y)$
		- Difficulty of finding collision = $2^{n/2}$ trials
			- To be secure it should be at least $2^{100}$
			- Easier due to [[Birthday Attack]] 
### Usage:
- **Integrity Check**: 
	- Hash functions are used to verify the integrity of transmitted data by comparing hash values before and after transmission.
	- [[Merkle Hash Tree]]
- **Password Protection**: 
	- Password hashed -> hash value stored
		- Storing the hash of a password instead of the password itself to prevent exposure in case of a security breach.
		- [[Dictionary Attack]]
		- [[Rainbow Crack]]
- **Message Authentication:**
	- Verifying the integrity of a message
		- Ensuring its content has not been altered by unauthorized parties. 
		- **Message Authentication Codes [[MAC]]**
	- Authentication and Confidentially is different things, should be handled separately
		- **Authenticated Encryption with Associated Data ([[AEAD]])**
	- It's crucial for the security of communications in networks.
### Real Life Examples:
- The properties that we discussed above was explanation for how ideal cryptographic systems should work.
- Real life examples of Cryptographic hash functions based on these properties:
	-  [[MD5]] (not considered as secure)
	- [[SHA-1]] (not considered as secure)
	- [[SHA-2]]
	- [[SHA-3]]

