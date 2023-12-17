### Definition:
- A part of the IEEE 802 Reference Model in [LAN](LAN.md)s
- Operates as a sublayer within the [Data Link Control Layer](Data%20Link%20Control%20Layer.md)
- Provides an interface between the Network Layer and the [Medium Access Control (MAC)](Medium%20Access%20Control%20(MAC).md) sublayer
### Properties:
- Provides an interface to higher layers.
- Manages flow control.
- Based on classical Data Link Control Protocols.
- Manages protocol multiplexing, flow control, and error checking.
- **Frame Format:**
	- Control field similar to HDLC's 16-bit version for I and S frames, and an 8-bit version for U frames
	- Avoids the primary/secondary station concept; all stations are peers
	- Conducts error detection using a 32-bit [CRC](Cyclic%20Redundancy%20Check%20(CRC).md) at the MAC layer.
	- Incorporates two levels of addressing: 
		- hardware addresses at the MAC layer
		- Service Access Point (SAP) identifiers at the LLC layer.
![MAC&LLC](Attachments/MAC&LLC.png)
### LLC Services:
- **Connection Mode**: 
	- Offers a connection-oriented service like [High Level Data Link Control (HDLC)](High%20Level%20Data%20Link%20Control%20(HDLC).md) ABM
	- involving error recovery and flow control.
- **Unacknowledged Connectionless:** 
	- Provides a quick data transmission method 
	- no connection setup, flow-control, error control, or ack
	- not reliable
	- suitable to use with [TCP-IP Protocol](TCP-IP%20Protocol.md)
- **Acknowledged Connectionless**: 
	- Ensures data integrity and reliability for single frames 
	- reliable
	- no connection setup -> no overhead

