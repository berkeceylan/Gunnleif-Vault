### Definition:
- Refers to the length of the shortest [[LFSR]] that can generate a given binary sequence
- It's a measure of the complexity and unpredictability of the sequence.
- denoted as $(L(s^n))$
### Importance:
- Linear complexity is used as a metric to evaluate the [[PseudoRandom |randomness]] or unpredictability of a sequence. 
- High linear complexity implies a higher level of unpredictability -> more suitable for cryptography usage
- [[BMA]] determine the linear complexity of a finite binary sequence.
### Properties:
- $\large L(s^n) = 0 \iff s_n$ is an all-zero sequence
- $\large L(s^n) = n \iff s_n = 0,0,\ldots,0,1$
- $\large L(s \oplus t) = L(s) + L(t)$
- $\large L(s \cdot t) = L(s) \cdot L(t) \implies \gcd(L(s), L(t)) = 1$