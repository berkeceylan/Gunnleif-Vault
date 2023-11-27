## ECB (Electronic Codebook)

### Definition:
- ECB is the simplest form of [Modes of Operations](Modes%20of%20Operations.md) to encrypt block cipher.
- Each block of plaintext is encrypted independently of any other block.
- It is a text book based idea.
	- its not secure and not used in real life
### How It Works:
- The plaintext is divided into n-bit blocks, and each block is encrypted with the same key. 
- If plaintext is not n-bit block -> padding is required
![](ECB.png)
### Properties:
- Each block encrypted/decrypted independently  from other blocks.
- There's no dependency between the blocks.
	- Encryption and decryption of each block independent.
- Error in single block do not propagate to other blocks.
- Loss of block does not affect decryption of other blocks.
- Very bad in image encryption
### Importance and Usage:
- **Cons**: 
	- Does not hide data patterns
		- Identical plaintext blocks -> identical cipher text blocks
		- [Substitution Cipher](Substitution%20Cipher.md)
	- Insecure for encrypting multiple blocks of identical data.
