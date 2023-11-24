### Definition:
- The birthday attack is a type of cryptographic attack that applies to hash functions and is named after the [birthday paradox](https://en.wikipedia.org/wiki/Birthday_problem) in probability theory.
- Used to find strong collisions in [[Cryptographic Hash Functions]] 
	- Reduces the trials $2^n$ to $2^{n/2}$
### How the Birthday Attack Works:
- Probability of finding a  strong collusion in a hash function
	- $P(2^n, k) > 1 - e^{-{k^2}/{2^{n+1}}}$
	- n =  number of hash values
	- k = number of messages used to find collisions
1. **Hash Function with a Finite Output Space**: Consider a hash function that produces $n$-bit hash values. There are $2^n$ possible hash outputs.
2. **Generating Hashes**: An attacker generates a large number of different inputs and computes the hash value for each one.
3. **Finding Collisions**: The attacker looks for pairs of inputs that have the same hash value. Due to the birthday paradox, finding a pair that collides requires only about $2^{n/2}$ attempts, which is the square root of the size of the hash function's output space.
### Relevance to Cryptographic Security:
- The birthday attack is significant because it shows that the security of a hash function against collision attacks is effectively halved in terms of bit strength. 
- To be protected by birthday attacks the output size should be larger to make it computably infeasible.
	- Larger $n$-bit
- Because of birthday attacks [[MD5]] and [[SHA-1]] not considered as secure.


