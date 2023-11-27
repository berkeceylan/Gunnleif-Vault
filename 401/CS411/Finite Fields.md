#MathBackground 
### Finite Fields (Galois Fields)
### Definition:
- GF is read as Galois field after a famous French Mathematician, Evariste Galois.
- A finite field or Galois field is a field that contains a finite number of elements.
- Finite fields are denoted as $\large GF(p^n)$
	- p is a prime number 
	- n is a positive integer.
- A special class in finite fields: [GF](GF.md)($2^n$)
- [Primitive Polynomials](Primitive%20Polynomials.md) : generates all the elements in a finite field
### Usage in Cryptography:
- Finite fields are used in various cryptographic algorithms
	- ECC (Elliptic Curve Cryptography)
	- [RSA](RSA.md) 
- They provide a set of elements with both addition and multiplication operations that have inverse operations for all non-zero elements.
### Operation:
- A field $GF(p)$ can be constructed using modular arithmetic:
	- $GF(p) = \{0, 1, \ldots, p-1\}$
- Operations in this field are performed modulo p