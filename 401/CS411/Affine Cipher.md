### Definition:
- Its one of the [[Classical Ciphers]]
-  Generalizes the [[Caesar Cipher]]
	- Caesar cipher is a specific case of the affine cipher
- One to one mapping exist
### Type:
- [[Symmetric Key Cipher]]  and [[Substitution Cipher]]
### Key: 
- Two integers (a multiplier and an addition value).
- $\large k = (\alpha, \beta) \text{ and } \alpha, \beta \in \mathbb{Z}_{26}$
### Operation: 
- Each letter in the plaintext is first multiplied by a number and then has another number added 
- Both operations modulo the size of the alphabet
- **Encryption**: 
	- $\large E_k(x) = y = \alpha \cdot x + \beta \mod 26$
- **Decryption**: 
	- $\large D_k(x) = x = \alpha^{-1} \cdot y + \gamma \mod 26$
		- $1/\alpha = \alpha^{-1}$
		- $\beta/\alpha = \gamma$
### Requirement: 
- The multiplier and the alphabet size must be co-prime.
- $\beta$ can be anything in the alphabet
- $\large gcd(\alpha, 26) = 1$ 
	- $\alpha$ = {1 ,3 ,5 ,7 ,9 ,11 ,15 ,17 ,19 ,21 ,23 ,25 }
	- If we not choose correctly
		- one-to one mapping between plaintext and ciphertext space broken
### Security: 
- Can be broken using frequency analysis and knowledge of the modulo arithmetic properties.
- Attack Types:
	- Ciphertext only
		- exhaustive search or frequency analysis
	- Known-plain Text
	- Chosen Plaintext
	- Chosen Ciphertext

