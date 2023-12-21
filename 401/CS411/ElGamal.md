### Definition:
-  Invented by 1985 by Taher ElGamal
- Based on [Discrete Logarithm (DL)](Discrete%20Logarithm%20(DL).md) problem on any finite [Group](Group.md)
- Ephemeral parameters (keys) = temporal key (parameters) not used in long time
	- Must be different for every message to be encrypted
### Encryption Protocol:
- The purple numbers are indicate that their matching steps in [Diffie-Helman Encryption Protocol](Diffie-Hellman%20Key%20Exchange.md#Encryption%20Protocol)
![ElGamalEncryption](../../Attachments/ElGamalEncryption.png)
### Efficient Implementation:
- **Setup Phase:**
	- Two primes:
		- p: 2048 bit
		- q: 224 bit
		- $G_q$: a subgroup of $Z_p^*$
			- q is generator of $G_q$
- **Key generation:**
	- Note: Visual implementation is above as a picture.
	- Generate random q => $2^{223} < q < 2^{224}$
	- Choose random integer  k => $2^{1823} \leq k \leq 2^{1824}$
	- p $\leftarrow$ kq +1
		- If p is not prime choose new k
		- If its prime continue
	- Choose random element $\alpha \in Z_p^*$
	- g $\leftarrow \alpha^{(p-1)/q} \mod p$ 
		- If g is 1 choose new $\alpha$
		- Otherwise create s and h
	- s (private key) : 1< s < q-1
	- h (public key) : $h = g^s \mod p$
- **Encryption:**
	- k random key 1 < k < q-1
	- $r = g^k \mod p$
	- $t = h^km \mod p$
	- (r , t): ciphertext
- **Decryption:**
	- $tr^{-s}$ \mod p
### Security:
- 'd' and 'i' (i.e. the private keys of Alice and Bob) so they must be kept in secret and chosen randomly for each message
- ElGamal is probabilistic algorithm since it randomly chooses different 'i' and 'd' for every encryption so it is a secure encryption algorithm
- Also similar as Diffie-Helman even since even an adversary find out the $K_E \text{ or } \alpha$ since finding KM is a discrete logarithm problem it can not be solved