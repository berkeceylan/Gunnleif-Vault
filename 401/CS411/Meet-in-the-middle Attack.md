Used to attack to [2DES](2DES.md) and [3DES](3DES.md) 
It reduce the amount of iteration while we generating key pairs.
**The Procedure:**
	1. **Forward Computation**:
	    - Choose a known plaintext and encrypt it with all possible values of $K_{1}$
	    - Store these results in a list.
	2. **Backward Computation**:
	    - Decrypt the known ciphertext with all possible values of $K_{2}$
	    - For each decryption, check if the result matches any value in the list created in step 1.
	3. **Matching**:
	    - If there is a match, then you've found a potential pair of keys ($K_{1}$,$K_{2}$) that could be the correct keys for the double encryption.