Mainly used in [Cryptography](Cryptography.md) applications
### Definition:
- Numbers generated using deterministic processes (often algorithms) that appear random.
	- Example: [Miller-Rabin Algorithm](Miller-Rabin%20Algorithm.md)
- Requires an initial value called a "seed" to start the generation process.
### Creation:
- **Software Based Random Number Generation**:
	- Algorithms designed to produce sequences that look statistically random.
	- Commonly used in computer systems due to ease of implementation.
	- Examples (weak):
		- The System Clock
		- Elapsed time between keystrokes or mouse movement
		- content of input/output buffers
		- user input
		- OS values
### Validation:
- **De-Skewing**:
	- If the initial output is biased or correlated
		- To fix biased output bits
		- Process of adjusting output of a generator to ensure uniform distribution
-  Created numbers should be checked by Pseudo-Randomness Tests like [FIPS](FIPS.md)
### Examples:
- Linear Congruential Generators (LCG).
- Mersenne Twister algorithm.
- Cryptographically Secure Pseudorandom Number Generators (CSPRNGs) 
	- like the Fortuna algorithm or Yarrow algorithm.