#MathBackground 
## Binary Finite Fields (GF)
### Definition:
- A binary finite field is a special case of the [Finite Fields](Finite%20Fields.md) $GF(p^n)$, where p = 2 
- Elements in this field can be represented as polynomials over $GF(2^n)$
### Usage in Cryptography:
- Binary finite fields are particularly useful in cryptography for error-correcting codes, such as those used in secure data transmission. 
- They are also used in [Block Cipher](Block%20Cipher.md) (design of S-boxes )and [Cryptographic Hash Functions](Cryptographic%20Hash%20Functions.md)
### Operation:
- A simple method to construct this field is to find all the binary polynomials whose degrees are smaller than the degree of the irreducible polynomial
- Each element in $GF(2^n)$ can be represented as a polynomial:
	- $a(x) = a_{n-1}x^{n-1} + a_{n-2}x^{n-2} + \ldots + a_1x + a_0$
	- Here,  $a_i \in GF(2)$, meaning each $a_i$ is either 0 or 1.
