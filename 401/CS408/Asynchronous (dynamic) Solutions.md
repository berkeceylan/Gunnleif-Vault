### Definition:
- A way of solving synchronization in channel allocation problem in [Media Access Control (MAC)](Media%20Access%20Control%20(MAC).md) sublayer.
- Idea: In response to immediate needs
- Used mainly where traffic patterns are unpredictable and vary over time.
- Based on:
	- dynamic allocation of resources
	- adapting to current network conditions
### Types:
### Round Robin Method
- **Definition**:
	- Each station in the network gets a turn to transmit data in a predetermined order
- **Properties**:
	- Turn is the time that one station can transfer data
		- can be decline or increase
		- created an overhead
	- Each station has equal access to the medium
		- reduce the chances of monopolization by a single station
		- fair
	- Minimizes collisions since each station knows its turn in the sequence
	- Perform well -> many station have data to transmit
	- Perform bad -> stations have no data to transmit during their turn
		- leading to wasted transmission opportunities
### Contention Method
- **Definition**: 
	- All stations contend to use the transmission medium
	- No control to determine whose turn is it
	- Stations sen data by taking risk of collusion with other packets
- **Properties**:
	- Stations transmit based on immediate needs, taking the risk of potential collisions.
		-  Stations can understand the collusion via listening the channel
		- If they realize a collusion they retransmit after random delay
	- Well-suited for environments with bursty traffic patterns
		- Bursty traffic: sending data continuously for some time and then remain idle for longer period of time
		- This type of traffic is typical traffic for most networks
	- Efficient -> under light or moderate load
		-  adaptable to varying network demands
	- Performance bad -> under heavy load
		- due to increased collisions and subsequent retransmissions
- **Applications**:
	- Commonly used in [Ethernet](Ethernet.md) networks under protocols like CSMA/CD (Carrier Sense Multiple Access with Collision Detection).

