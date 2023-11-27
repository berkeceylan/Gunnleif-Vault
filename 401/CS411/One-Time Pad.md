## One-Time Pad
### Definition:
- Type of a [cryptographic](Cryptography.md) encryption algorithm
- Theoretically unbreakable system
- Each bit of the plaintext is encrypted with a corresponding random bit from a key that is as long as the message itself
### Type:
- [Asymmetric Key Cipher](Asymmetric%20Key%20Cipher)
### Properties & Requirements:
- The key must be a truly random sequence of bits or characters.
- It needs to be as long as the plaintext message.
- Each key must be used only once and never reused for any other message.
### Operation
- Combining each bit or character of the plaintext with the corresponding bit or character of the key using the XOR operation
### Security
- It's know as unbreakable system
	- The encryption is unbreakable due to its unbiased and unpredictable key generation:
	- The probability of a '1' or '0' occurring in the key is truly random (P(0) = P(1) = 1/2).
	- The key is independent of the number of bits, making the prediction of the next bit (whether 0 or 1) impossible.
- No diffusion
- Confusion is achieved due to the inherent [randomness](PseudoRandom.md) of the key
