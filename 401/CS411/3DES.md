## Triple Data Encryption Standard (Triple DES )
### Description:
* Also known as Triple DES
* Derived from the Data Encryption Standard ([[DES]]) block cipher
* Triple DES applies the DES algorithm three times, with different keying options:
	* **Keying Options**
		- ***3-Key Triple DES**: 
			- All three keys are independent. 
			- This provides an effective key length of 168 bits.
		- **2-Key Triple DES**: 
			- $K_{1}$  and $K_{3}$  are the same, and $K_{2}$ is different.
			- This gives an effective key length of 112 bits.
			- Used more since it can be directly adapted from single DES
		- **1-Key Triple DES**: 
			- All three keys are the same
			- Reverting the operation effectively back to standard DES.
			- Not used since it is open the same attack done towards DES
* ==Effective key length = 112 bits==
* Since block size is fixed and 64-bit blocks to encrypt larger data blocks we use [[Modes of Operations]]
### How It Works:
**Encryption**:
$\text{Ciphertext} = E_{K3}(E_{K2}(E_{K1}(\text{Plaintext})))$ 
or
**More valid one:** $\large \text{Ciphertext} = E_{K1}(D_{K2}(E_{K1}(\text{Plaintext})))$ 

**Decryption**:
$\text{Plaintext} = D_{K3}(D_{K2}(D_{K1}(\text{Ciphertext})))$ 
or
**More valid one:** $\large \text{Ciphertext} = D_{K1}(E_{K2}(D_{K1}(\text{Ciphertext})))$ 
### Security:
- Again key length may be seem as 168 bits (56 bits + 56 bits +56bits ), however because of [[Meet-in-the-middle Attack]] effective key length reduced to 112bits.
- Triple DES is considerably secure , however there are more secure and efficient algorithms like [[AES]] in both hardware and software.
