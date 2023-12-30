## TCP (Transmission Control Protocol)
### Definition:
- Connection-oriented protocol ensuring data is sent and received reliably.
- One of the protocols of [TCP-IP Protocol](401/CS408/TCP-IP%20Protocol.md) suite
- Defined in RFC 793
- **Properties:**
	- Ensures end-to-end communication
	- Manages data packet assembly before transmission, and reassembly
	- Provides error-checking to ensure data integrity.
	- Reliable
### Properties:
-  Service Primitives:
	- Items passed to IP
	- Payload length
		- TCP Payload Length = Total Length - (IP Header Length + TCP Header Length)
- Difficulties: (Do not use this name)
- Special Capabilities:
### Connection Management:
### Operation

### TCP Header
- **CheckSum:**
- **Maximum Segment Size:**
- **Window Scale:**
- **Sack-permitted:**
- **Sack:**
- 
![](Attachments/TCP.png)
### Mechanisms:
### Policies:
- **Send policy:**
- **Deliver policy:**
- **Accept policy:**
- **Retransmit policy:**
- **Acknowledge policy:**