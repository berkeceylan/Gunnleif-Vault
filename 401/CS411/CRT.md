#MathBackground 
## Chinese Remainder Theorem (CRT)
## Definition:
- Allows determination of an unknown integer from its remainders when divided by several pairwise coprime integers.
## Theorem: 
- Provides a solution to a system of linear congruences with pairwise coprime moduli.
- $x \equiv a_i \mod n_i$
- We can use [Gaus Algorithm](Gaus%20Algorithm.md) based on CRT
## Usage in Cryptography:
- CRT is used in [RSA](RSA.md) algorithm to speed up calculations for decryption and signing by working with smaller numbers.