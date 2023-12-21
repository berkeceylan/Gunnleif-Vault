#MathBackground 
### Definition:
- A primitive root of a [Group](Group.md) is an element that generates every other element of the group when repeatedly applied under the group operation.
- Also called primitive elements or multiplicative generators
### Properties & Example 
- Consider powers of 3 mod 7:  
	- $3^1 \equiv 3, 3^2 \equiv 2,3^3 \equiv 3^4 \equiv 4,3^5 \equiv 5,3^6 \equiv 1$ in mod 7
	- Powers of 3 generate all nonzero elements of the congruence class mod7.
- Such elements are called primitive elements or multiplicative generators in the congruence class.
- If p is a prime, there are $\phi(p − 1)$ primitive elements mod p.
	- To look what is $\phi(n)$ go -> [Euler’s Theorem](Euler’s%20Theorem.md)
### Usage in Cryptography:
- Primitive roots are used in primitive element theorem-based systems like:
	- [Discrete Logarithm (DL)](Discrete%20Logarithm%20(DL).md)
	- [Diffie-Hellman Key Exchange](Diffie-Hellman%20Key%20Exchange.md)