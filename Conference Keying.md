### Definition:
- Make possible secure key distribution for n people in a efficient way
- Based on [Diffie-Hellman Key Exchange](401/CS411/Diffie-Hellman%20Key%20Exchange.md)
### Operation:
- **Setup:**
	- We have t users
	- Prime p and q -> p > q
	- Generator g in $G_q$
- **Partial Key Generation:**
	- User $U_i$ selects a random integer $1 < r_i < q$
	- User $U_i$ computes $z_i = g^{r_i} \mod p$
	- User $U_i$ sends $z_i$ to $U_{i-1 \mod t} \text{ and } U_{i+1 \mod t}$
- **Computation of key:**
	- Each user $U_i$ after receiving $z_{i-1} \text{ and } z_{i+1}$ computes
		- $\large x_i = g^{r_{i+1}r_i-r_{i-1}r_i}$
	-  Each user $U_i$ broadcast $x_i$
	- After receiving $x_j -> 1 \leq j \leq t -> j \neq t$
	-  Each user $U_i$ computes
		- $K = (z_{i-1}^{tr_i})(x_{i}^{t-1})(x_{i+1}^{t-2})\dots(x_{1}^{i+(t-1)})\mod p$
![](Attachments/MultipartyDHKey%20Exchange.png)