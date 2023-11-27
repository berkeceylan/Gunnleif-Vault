## Teletype Network (Telnet)

### Historical Context:
- Telnet is the oldest Internet application.
- First published version RFC 97.
	- First Cut at a Proposed Telnet Protocol"
- Final form RFC 854 and RFC 855.
- It's an application-level protocol designed by Jon Postel.
### Properties
- Oldest [Internet](Internet) application.
-  Telnet operates at the [Application Layer](Application%20Layer.md).
- Basis of newer protocols, such as [HTTP](HTTP.md).
- Telnet is a protocol designed to provide [Remote Terminal Access](Remote%20Terminal%20Access.md) over a [TCP/IP](TCP/IP) network.
- Telnet operates on the principle of the Network Virtual Terminals ([NVT](NVT.md))
- Telnet uses TCP on port 23
- **Advantage:** Low transmission overhead 
	- No message headers
- **Disadvantage:** High processing overhead
	- Due to char by char processing
- Telnet is not a secure protocol 
	- Therefore [SSH](SSH) became a standard since it is secure
### Phases of Operation:
1. **Connection Management**:
	- Initiating and terminating connections using TCP on port 23.
2. **Negotiation**:
	- Establishing a set of agreeable characteristics and options.
	- There are different options:
		- Every option is 3 Byte
			- 255 / option / ID of the option
		- Not part of Telnet protocol specification
		- Enable two sides to use capabilities beyond [NVT](NVT.md)
		- [Option Negotiation](Option%20Negotiation.md)
	- Options are not enabled until negotiation is complete.
		- There should be mutual agreement
1. **Exchange Data** 
	- Data is transmitted in multiple rounds as a stream of bytes
		- Each byte is processed one by one
		- Increase processing overhead
	- No application-level packet structure.
	- Commands are embedded in data stream
		- Via "Interpret as Command" (IAC) = 255
		- Minimizes transmission overhead 
2. **End Session**: 
   -  TCP connection terminates

