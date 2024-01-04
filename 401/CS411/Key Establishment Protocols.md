#NotFinished 
### Definition:
- **Problem:**
	- Distribution and the security of the keys is a big problem
	- Even the algorithm is secure we may unable to distribute or protect keys over a network
- **Solution:**
	- Using [PKC](PKC.md) -> not suitable multiple(n>2) user
	-  [Conference Keying](Conference%20Keying.md)  -> suitable for multiple(n>2) user
	- Using [Diffie-Hellman Key Exchange](Diffie-Hellman%20Key%20Exchange.md)
		- Do not provide authentication -> [Man-in-the-Middle Attack](Man-in-the-Middle%20Attack.md)
	- [Station-to-Station Protocol](Station-to-Station%20Protocol.md) -> authenticated version of DH
		- Has [Forward Secrecy](Forward%20Secrecy.md)
	- 
### Key Distribution:

