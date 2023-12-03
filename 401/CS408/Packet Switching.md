## Packet Switching
### Defintion:
- A type of [Switching](Switching.md) in WANs
- Method of data transmission where information is sent in small units called packets over a shared network
### Operation:
- Data transmitted in short blocks (packets)
	- data + header with control info (has destination station address)
	- store and forward technique: Each node
		-  packet received
		- stored briefly
		- processed (determines next leg of route)
		- passed to next node/ queue to packet to go
### Types: 
- There are two types of packet switching:
	- [Datagram](Datagram.md)
	- [Virtual Circuit](Virtual%20Circuit.md)
	
| Feature | Virtual Circuits | Datagram |
|---------|------------------|----------|
| **Sequencing and Error Control** | Provided by the network | Handled individually by end systems |
| **Packet Forwarding Speed** | Faster, as no routing decisions are needed per packet | Slower, as each packet may require routing decisions |
| **Reliability and Flexibility** | Less reliable and flexible | More reliable and flexible |
| **Impact of Node Loss** | Loss of a node disrupts all circuits through that node | Alternate routes can be found; resilience to node failure |
| **Call Setup Phase** | Required | None, packets are sent individually |
| **Suitability for Traffic** | More efficient for steady streams of packets | Better for sporadic and few packets |
| **Congestion Response** | Not responsive to congestion | Can reroute to avoid congestion |

## Total Delay:
- Total delay: time needed for data to go from the sender to receiver
- Round Trip  Time Delay(RTT): total delay + time needed to acknowledgment (ACK)
- Assume: N packets and k intermediate switching node
	- Transmission Time: (N+k) x Ttrans
	- Propagation Time: (k+1) x Tprop
	- Processing Time: k x Tproc
	- Total : (N+k) x Ttrans + (k+1) x Tprop +  k x tproc
## Pros & Cons:
- **Pros**
	- Line efficiency
		- No dedicated capacity
	- Data rate conversion
		- each node as own speed
	- Queue System
		- Even network is busy packets can accepted
- **Cons**
	- Not a smooth process (data rate is not fixed)
	- Delay
		- Processing Delay
			- Time it takes for a node to process the packet header
			- More processing needed
		- Variable Delay
			- Due to processing and queuing
		- Transmission Delay
			- Time taken to push all the packet's bits onto the link
			- Link Bandwidth (in bps) / Packet Size (in bits)
		- Propagation Delay
			- Time taken for a signal (or bit) to travel from the sender to the receiver
			- The Length of Channel (Distance) / Propagation Speed
	- Header Overhead: header transferred but don't have the app data



