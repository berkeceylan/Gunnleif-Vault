### Definition:
- Most popular [[PKC]]
- Invented by Rivest, Shamir, and Adleman in 1977
- Based on Integer Factorization
	- bit length = 2048/3072/7680/15360
### Type:
- [[Asymmetric Key Cipher]]
### Properties:
- Each user has public and private key pair
- Keys are generated based on the product of two large prime numbers
- The operation based on [[Fermat’s Little Theorem]] and [[Euler’s Theorem]]
- provides non-repudiation in digital signatures
- Public Key: $(e , n)$
- Private Key: $(d,p,q)$
### Operation:
- **Setup Stage**:
	1. Choose two large primes p and q
		- We use  [[Miller-Rabin Algorithm]] for primality testing
		- While we do primality test we need to pay attention to [[Distribution of Primes]]
	2. Compute $n = p \times q$
	3. Compute $\phi(n) = (p-1) \times (q-1)$
	4. Choose a random integer, $0 < e < \phi(n)$ with $gcd(e,\phi(n)) = 1$
	5. Compute the inverse $d = e^{-1} \mod \phi(n)$  i.e.  $e \times d = 1 \mod \phi(n)$
	- Then we get:
		- Public Key: $(e , n)$
		- Private Key: $(d,p,q)$
- **Encryption**:
	- done by using public key
	- $\large y = x^e \mod n, \text{ where } x < n$
- **Decryption**:
	- done by using private key
	- $\large x = y^d \mod n$
### Security:
- Brute force attack is practically impossible
- Finding $\phi(n)$ difficult as factoring n
- Factoring n -> only practical approach
	- **Quadratic Sieve (QS):**
		- Speed depends on the size of the modulus n
		- 129 digit ($\approx$ 428 bits) is broken by QS in 1994
		- Complexity : $O\left(e^{(1+o(1))\sqrt{\ln(n)} \ln(\ln(n))}\right)$
	- **Elliptic Curve Method:**
		- Speed depends on the size of the smallest factor of n = p and q
		- So choosing sizes of p and q similar to each other crucial for RSA security
		- Complexity: $O\left(e^{(1+o(1)) 2 \ln(p) \ln(\ln(p))}\right)$
	- **Number Field Sieve(NFS):**
		- Asymptotically better than QS
		- 140 digit ($\approx$ 465 bits) is broken by QS in 1999
		- Complexity: $O\left(e^{(1.92+o(1))(\ln(n))^{1/3} (\ln(\ln(p)))^{2/3}}\right)$
			- Currently largest number factored so far is use NFS method($\approx 768$ bit)
	- **Side Channel Attacks:**
		- Based on voltage peaks in [[Modular Exponentiation]] during decryption.
			- Observe the voltage peaks in decryption process caused and find 0's and 1's in the d then find d.
			- This method called [Simple Power Analysis (SPA)](https://en.wikipedia.org/wiki/Power_analysis)
		- **Countermeasure Agains SPA:**
			- Text-based RSA is deterministic so it is not protected from SPA
			- If we add randomization to RSA algorithm:
				- Ensure [[Semantic Security]]
				- Protect from SPA
			- This randomization can be created via: 
				- **Optimal Asymmetric Encryption Padding ([[OAEP]])**
					- Detailed information about [OAEP](https://en.wikipedia.org/wiki/Optimal_asymmetric_encryption_padding)
				![[RSAOAEP.png]]