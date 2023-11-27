#MathBackground 
## Greatest Common Divisor (GCD)
### Definition:
- The largest positive integer that divides two or more integers without leaving a remainder.
### Theorem: 
- If a and b are integers, not both zero, there exist integers x and y such that 
- $ax + by = gcd(a,b)$
- When $gcd(a, b) = 1$, they are relatively prime
	- Equation becomes $ax + by = 1$
	- Multiplicative inverse: $ax \equiv 1 \mod b$
- [Euclidean Algorithm](Euclidean%20Algorithm.md) is a method to find large numbers GCD
###  Usage in Cryptography:
- The GCD is used in algorithms to find multiplicative inverses, which are crucial for decryption and digital signatures.