## TCP (Transmission Control Protocol)
### Definition:
- Connection-oriented protocol ensuring data is sent and received reliably.
- One of the protocols of [TCP-IP Protocol](401/CS408/TCP-IP%20Protocol.md) suite
- **Properties:**
	- Ensures end-to-end communication
	- Manages data packet assembly before transmission, and reassembly
	- Provides error-checking to ensure data integrity.
	- Reliable
### Design Issues (assume reliable IP ):
- **Addressing and Multiplexing:**
	- Multiple application protocol uses one transport layer
		- Users are multiplexed
		- User id locally identified via port number
	- User Identification -> host address & port -> socket
		- Port = particular transport service(TS)
		- Host address = attached network device
- **Flow Control:**
	- End-to-end
	- Receiver may not keep up with the flow of data -> "buffers filling up"
	- Harder than Link-level flow control -> delay is bound tı network -> difficult to use timeout
	- **Methods:**
		- **Do nothing:**
			- overflow -> discard segments (packets)
			- fail to get ACK -> retransmit
			- not good for reliability
		- **Backpressure:**
			- Refuse further segments at link or network layer ->propagate until to sender
			- Course grained approach since we cannot identify the problematic network
		- **Sliding Window + Credit scheme:**
			- similar to [Sliding Window](Sliding%20Window.md)
				- sender sends up to certain window size without getting ack
					- credits give the sender permission to send a certain amount of data, regardless of whether previous data has been acknowledged.
				- window size set dynamically (bytes)
			- Credit scheme prevents the sender from overloading the receiver's buffer
				- flow control is managed independently of the packet ack process
				- each segment has header like:
					- sequence number -> each byte has unique sequence number
					- ack number
					- window size 
				- segments are numbered with the sequence number of their first byte
- **Connection Establishment/Termination:**
	- necessary even with reliable network services
	- mutual agreement -> control messages are exchanged
	- purpose:
		- allow each end user yo know the other exist and willing to communicate
		- negotiation of optional parameters
		- trigger allocation of transport entity resources

### TCP Header
![](Attachments/TCP.png)
