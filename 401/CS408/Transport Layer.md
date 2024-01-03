### Definition:
- Fourth Layer of [OSI Model](OSI%20Model.md) (Open Systems Interconnection)
- Corresponding the transport layer in [TCP-IP Model](TCP-IP%20Model.md)
- Provides end-to end data transfer
- Shields upper layer application protocols from the details of networks
- Two types:
	- Connection Based:
		- Logical connection between end users
			- Connection Establishment
			- Data Transfer
			- Connection Termination
		- Reliable Service
	- Connectionless:
		- Unreliable
- Two main protocols:
	- [TCP](TCP.md): 
		- Complicated flow and error control since the [Network (IP) Layer](Network%20(IP)%20Layer.md) is unreliable
		- Complex
		- Connection oriented
	- [UDP](UDP.md):
		- Basic 
		- Connectionless
### Design Issues:
- Assume Reliable Network Service: [Reliable Network Service in TL](Reliable%20Network%20Service%20in%20TL.md)
- Assume Unreliable Network Service: [Unreliable Network Service in TL](Unreliable%20Network%20Service%20in%20TL.md)
	- Usual Case -> uses IP

