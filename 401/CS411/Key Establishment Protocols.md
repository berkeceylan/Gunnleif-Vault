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
- Problem with key pre-distribution protocols:
	- Keys are predetermined and not easily changed
	- Keys must be changed after certain time
- Solution: Transport protocols
	- A class of key establishment protocols
	- Two approaches:
		- One party to decide on a key and transmit it to other
		- A trusted authority will act as a key server
			- [[Authentication using Symmetric Encryption]]

