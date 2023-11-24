## Authenticated Encryption with Associated Data (AEAD)
### Definiton:
- Encryption systems that simultaneously protect confidentiality and authenticity of communications
- Based on [[AES]] and [[Cryptographic Hash Functions]]
	- Encryption Scheme + [[MAC]]
### Types
- **Encrypt-then-MAC(EtM)**:
	- Provide message authentication and confidentially in same time
	- Authentication is tied to ciphertext
	- Can be parallelized
	![[EtM.png]]
- **MAC-then-Encrypt(MtE)**:
	- Provide message authentication and confidentially in same time
	- Authentication is tied to ciphertext
	- Cannot be parallelized
	![[MtE.png]]
- **Encrypt-and-MAC(E&M)**:
	- Provide message authentication and confidentially in same time
	- Authentication is tied to ciphertext
	- Sender can parallel but Receiver can not parallel
	![[EandM.png]]