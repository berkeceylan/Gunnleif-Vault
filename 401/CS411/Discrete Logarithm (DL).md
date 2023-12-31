### Definition:
- DL is the underlying hard problem for:
	- [Diffie-Hellman Key Exchange](Diffie-Hellman%20Key%20Exchange.md)
	- [Digital Signature Algorithm (DSA)](Digital%20Signature%20Algorithm%20(DSA).md)
	- [ElGamal](ElGamal.md)
	- [Elliptic Curve Cryptography (ECC)](Elliptic%20Curve%20Cryptography%20(ECC).md)
- DL is defined over finite [Group](Group.md)s
- **Problem Definition:**
	- Let p be a prime and $\alpha$ and $\beta$ be nonzero integers in $Z_p$ and suppose.
		- $\beta = \alpha^x \mod p$ 
			- $\alpha$ is usually a primitive root of $\mod p$
			- $0 \leq x \leq p-1$
			- $Z_p$ is a finite field $0,1,\dots,p-1$
			- $Z_p^*$ is a cyclic finite group $1,\dots,p-1$
		- The problem finding x is called discrete logarithm problem
			- Finding x is hard however finding x is even or odd is easy
			- To detailed info look at the DL slide page9 and 10
				- [CS411_507_Ch8_PKC2_DL_202301_handout](Attachments/CS411_507_Ch8_PKC2_DL_202301_handout.pdf)
	- If p is > 200 -> it is hard as factorization problem
	- One way function:
		- Calculating modular exponentiation is easy
		- Calculating discrete log(i.e. inverse of modular exponentiation) is hard
### Attacks:
- **Shanks's Algorithm:**
	- Baby step giant-step
	- DL in $Z_p^*:(p)^{1/2}$ steps
	- Minimum security requirement: $(p-1) > 2^{224}$
- **Pohling-Hellman Algorithm:**
	- $|Z_p^*| = p_1p_2p_3 \dots p_j$
	- Minimum security requirement: $(p-1) > 2^{224}$
	- Complexity: $O((p_j)^{1/2})$
- **Index-Calculus Method:**
	- Applies only to $Z_p$ and $GF(p^k)$
	- Minimum security requirement in $Z_p^*: (p-1)> 2^{2048}$
	- Complexity: $O(e^{(1+O(1)\sqrt{ln(p)ln(ln(p))})})$
