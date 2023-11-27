## Definition:
- To encrypt larger data blocks then the block size of [DES](DES.md), [3DES](3DES.md) and [AES](AES.md) we use this method.
	- [Block Cipher](Block%20Cipher.md) methods only encrypt single block but in real life we decrypt larger data blocks.
	- To solve this problem modes of operations used, it make possible larger data blocks encrypt securely.
- NIST defines 5 modes can be used with any block cipher.
	- ECB is not used in real life its insecure
- There are different mode types that can be used with DES and AES
## Types:
- Electronic Codebook ([ECB](ECB.md))
	- Text book based
	- Insecure
- Cipher Block Chaining([CBC](CBC.md))
	- CBC + AES = Semantic Security
- Cipher Feedback([CFB](CFB.md))
	- Stream cipher mode
- Output Feedback([OFB](OFB.md))
	-  Stream cipher mode
- Counter([CNT](CNT.md))
### Comparison Summary:
| Mode        | Type          | Dependency     | Sync           | Parallelization | Error Propagation | 
|-------------|---------------|----------------|----------------|-----------------|-------------------|
| ECB         | Block         | Independent    | Not Applicable | Yes             | No                | 
| CBC         | Block         | Dependent      | Self-Sync      | Decryption only | Yes               | 
| CFB         | Stream        | Dependent      | Self-Sync      | No              | Limited           |
| OFB         | Stream        | Independent    | Not Applicable | Yes              | No                | |
| CNT         | Stream        | Independent    | Not Applicable | Yes             | No                | 


