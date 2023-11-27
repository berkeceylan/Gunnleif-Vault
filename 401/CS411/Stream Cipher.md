### Definition
- Type of a [cryptographic](Cryptography.md) encryption algorithm
- Basic idea comes from [One-Time Pad](One-Time%20Pad.md)  
- Plaintext digits are combined with a pseudorandom cipher digit stream (key stream)
- Each plaintext digit is encrypted one at a time with the corresponding digit of the key-stream, to give a digit of the ciphertext stream
- **Example(s):**
	- Salsa20
	- A5/1 (used in GSM)
	- Trivium
- There are two type of Stream Ciphers:
	- [Synchronous Stream Ciphers](Synchronous%20Stream%20Ciphers.md)
	- [Asynchronous Stream Ciphers](Asynchronous%20Stream%20Ciphers.md)
### Type:
- [Symmetric Key Cipher](Symmetric%20Key%20Cipher.md)
### Key:
- Typically shorter than the plaintext.
- Key-stream is generated using [PseudoRandom](PseudoRandom.md) generator form a relatively short secret key
- To produce key we use [LFSR](LFSR.md), it provide:
	- Large period
	- Good statistical properties 
	- Large linear complexity
- ![](StreamCipher.png)
### Operation:
- Encryption:
	- $\large c_i = m_i \oplus k_i$
- Decryption:
	- $\large m_i = c_i \oplus k_i$
### Security:
- If key stream is not reused secure against known plaintext attacks
	- Vulnerable if key stream is reused
- Security reduces if parts of the key stream can be predicted
	- Unbiased
		- Ideally, in a secure stream cipher, the chance of a '1' or '0' in the key stream should be roughly equal: P(0) ≈ P(1) ≈ 1/2.
	- Predictability
		- Predicting the next bit in the key stream should be computationally infeasible
		- probability of guessing should be close to 1/2 for either a '0' or '1'.
	- **[BMA](BMA.md)**:
		- It can determine the shortest LFSR (i.e., the feedback polynomial of the LFSR) that can produce a given binary sequence.
		- By using BMA we can attack the Stream Cipher and break
- Correlation and Brute Force attacks possible
	- Cost of Correlation Attack: $\prod_{i=1}^{n} (2^{L_i} - 1)$
	- Cost of Brute Force Attack: $\sum_{i=1}^{n} (2^{L_i} - 1)$
- Diffusion: 
    - Not explicitly present, as each plaintext bit affects only one ciphertext bit
- Confusion:
    - Achieved inherently due to the [PseudoRandom](PseudoRandom.md) of the key-stream

