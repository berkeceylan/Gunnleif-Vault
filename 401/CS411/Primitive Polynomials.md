#MathBackground 
### Definition:
- A primitive polynomial is a polynomial that generates all elements of a [Finite Fields](Finite%20Fields.md) as its roots when used in a polynomial sequence.
- The root of some of the irreducible polynomials can be used to construct the binary extension field ([GF](GF.md)).
	- means it generates all possible non-zero elements of the field.
### Usage in Cryptography:
- Primitive polynomials are essential in constructing binary finite fields, which are used:
	- Advanced Encryption Standard ([AES](AES.md)). 
- They ensure that the algebraic structures have the desired properties for secure and efficient computation.
### Operation:
- The general form of a primitive polynomial in $GF(2^n)$ can be written as:
	- $p(x) = x^n + a_{n-1}x^{n-1} + \ldots + a_1x + 1$
- The coefficients $a_i$ are elements of GF(2), meaning each $a_i$ is either 0 or 1, and 
- Root of a primitive polynomial is called primitive element.
