### Definition:
- A three-party [key distribution protocol](401/CS411/Key%20Establishment%20Protocols.md)
- For session between A and B, mediated by a trusted [Key Distribution Center (KDC)](401/CS411/Key%20Distribution%20Center%20(KDC).md)
	- KDC should be trustworthy since it knows the session key
### Operation:
- $A -> KDC: ID_A||ID_B||N_1$
- $KDC -> A: E_{K_A}(K_S||ID_B||N_1||E_{K_B}(K_S||ID_A))$
	- $E_{K_B}(K_S||ID_A)$ part cannot be decrypted by A so it send s it to B
	- KDC sends that part A to reduce transmitted message amount
- $A -> B: E_{K_B}(K_S||ID_A)$
- Handshake part -> prevent replay attack (DDOS)
	- $B -> A E_{K_S}(N_2)$
	- $A->B: E_{K_S}(f(N_2))$
- This method still vulnerable to attacks since if the attacker learn $E_{K_B}(K_S||ID_A)$ it can present itself as A and learn future communications.
### Operation with Timestamp
- $A -> KDC: ID_A||ID_B||N_1$
- $KDC -> A: E_{K_A}(K_S||ID_B||N_1||E_{K_B}(K_S||ID_A||T))$
- $A -> B: E_{K_B}(K_S||ID_A||T)$
- $B -> A E_{K_S}(N_1)$
- $A->B: E_{K_S}(f(N_1))$
- A and B can understand replays by checking the timestamp in the message
- Even the attacker find out $K_S$ he cannot generate $E_{K_B}(K_S||ID_A||T)$ with a fresh timestamp since he/she did not know encryption key ($K_B$)