#MathBackground 
### Definition: 
- Two integers a and b are congruent modulo n if they have the same remainder when divided by n.
- $a \equiv b \mod n$
### Theorem: 
- If $\large a \equiv b \mod n$ and $\large c \equiv d \mod n$ , then
	- Addition: $a + c \equiv b + d \mod n$
	- Multiplication: $ac \equiv bd \mod n$
### Proposition: 
- If $gcd(a, n) = 1$, then there exists an integer s such that $(as \equiv 1 \mod n)$
	- Multiplicative inverse: $a \cdot s \equiv 1 \mod n$
### Usage in Cryptography:
- Congruences are used in modular arithmetic, which is fundamental for encryption algorithms and [Cryptographic Hash Functions](Cryptographic%20Hash%20Functions.md)