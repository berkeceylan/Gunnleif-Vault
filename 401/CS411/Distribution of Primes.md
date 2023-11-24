It is a important Concepts when we generate large prime numbers in [[RSA]]
### Problem:
- How many integers are likely to be rejected before a prime number is found using a primality test ?
### Observation:
- Prime Number Theorem: Let $\pi(n)$ be the # of primes less than x. Then $\pi(n) -> x/lnx$
	- i.e. primes near x are spaced, on the average, one every $(ln x)$
	- so we need to test $ln x$ integer before find prime number
- However we can reduce even numbers (half of the numbers 0.5) and numbers end with 5 (0.1) since we know that they are not prime.
- So at the end we only need $0.4 \times ln x$ trials