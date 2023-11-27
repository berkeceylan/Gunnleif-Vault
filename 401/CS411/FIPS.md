## Federal Information Processing Standards (FIPS)

### Definition:
- A suite of tests to ensure the [randomness](PseudoRandom.md) of cryptographic sequences.
- Established by the NIST 
### Types of Randomness Tests:
- **Poker Test**:
	- A sequence is divided into k non-overlapping segments of length m
	- This test determines if each segment of length m appears approximately the same number of times
- **Monobit (frequency) Test**: 
	- To check if the number of 1's and 0's in a sequence is the same
- **Runs Test**:
	- Designed to analyze the occurrence of consecutive bits (runs) in a given binary sequence. 
	- A run is a sequence of consecutive bits with the same value (either all 0s or all 1s).
	-  Determines if the # of runs of various lengths is similar to those of truly random sequences for a random sequence
- **Long Run Test**:
	- To check if the sequence contains any 34 consecutive of zeros or ones
	- If it exist test fails, otherwise passes