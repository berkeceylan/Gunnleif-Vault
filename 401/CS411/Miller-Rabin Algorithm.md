### Definition:
- Probabilistic algorithm 
	- Very efficient and fast
- Used to determine whether a number is prime heavily in [RSA](RSA.md)
- It provides a probabilistic result
- It can identify a number as either a composite (definitely not prime) or a probable(pseudo prime) prime.
- To check how we generate large prime numbers check [Large Prime Numbers in RSA](https://www.geeksforgeeks.org/how-to-generate-large-prime-numbers-for-rsa-algorithm/)
### Operation:
- TEST:
	- Input: n
	- Output:
		- n is composite -> %100 assurance
		- n is probably prime -> %75
- Repeat this TEST
- If, at any point, the TEST returns “composite” -> n = nonprime
- If the TEST returns “inconclusive” t times ->  the probability that n is prime is at least $(1-4^{-t})$
