## Definition:
- To encrypt larger data blocks then the block size of [[DES]], [[3DES]] and [[AES]] we use this method.
	- [[Block Cipher]] methods only encrypt single block but in real life we decrypt larger data blocks.
	- To solve this problem modes of operations used, it make possible larger data blocks encrypt securely.
- NIST defines 5 modes can be used with any block cipher.
	- ECB is not used in real life its insecure
- There are different mode types that can be used with DES and AES
## Types:
- Electronic Codebook ([[ECB]])
	- Text book based
	- Insecure
- Cipher Block Chaining([[CBC]])
	- CBC + AES = Semantic Security
- Cipher Feedback([[CFB]])
	- Stream cipher mode
- Output Feedback([[OFB]])
	-  Stream cipher mode
- Counter([[CNT]])
