### Definition:
- Passes routing information between routers within Autonomous Systems
- Need exchange of info among the routers only in Autonomous Systems
- Different autonomous systems may have different IRP mechanisms
### Protocols:
### RIP (Routing Information Protocol):
- Based on [Distance-Vector Routing Method](Routing.md#Distance-Vector%20Routing%20Method)
	- Each node exchanges information with neighbors
	- Neighbor = Directly connected via same network
- Each node maintains three vectors
	- Link cost
		- One entry for each network it attaches
	- Distance vector (metric column in routing Table)
		- Current cost of route from the node to each destination network
	- Next hop vector (next router column in routing table)
		- The next router for each destination network
- Every 30 seconds -> exchange distance vector with neighbors
- Use distance vectors received from neighbors to update distance and next hop vector
- RIP uses UDP that means no reliability and there is no synchronization
- RIP is designed to operate incrementally
	- Tables are updated after receipt of individual distance vector
-  If no updates are received from a router within 180 seconds, mark the connection as invalid
	- Assumes router crash or network connection unstable
	- Set distance value to infinity (16)
	- if convergence is slow = [Counting Infinity Problem](https://www.geeksforgeeks.org/route-poisoning-and-count-to-infinity-problem-in-routing/)
- Split Horizon rule => do not send information about a route back in the direction it came from
	- solves counting infinity problem
- Similar to Bellman-Ford algorithm
### OSPF (Open Shortest Path First):
- Based on [Link-State Routing Method](Routing.md#Link-State%20Routing%20Method)
- RIP has limitations in large internets
	- Convergence problem (May led to counting infinity problem)
	- RIP metrics are very simple and might cause suboptimal routes to be formed
- OSPF is preferred interior routing protocol for [TCP-IP Protocol](TCP-IP%20Protocol.md) based internets
- Router maintains the state (i.e. cost) of local links
- Transmits updated state information to all routers in [Autonomous Systems (AS)](Autonomous%20Systems%20(AS).md) or in [Area](Area.md) 
- Router receiving update must acknowledge
- Each router maintains a database that reflects the topology
	- Directed graph
		- Vertices (nodes)
			- Routers
			- Networks
		- Edges
			- Connecting two routers
			- Connecting router to network
	- Generates a spanning tree and routing table
- Link Costs:
	- Cost of each hop in each direction = routing metric
	- OSPF provides flexible metric scheme based on type of service
		- Normal
			- Default metric assigned by administrators
			- Typically 1 for minimum hop routing
		- Monetary cost
		- Reliability -> based on recent history of outages
		- Throughput -> Inversely proportional to data rate
		- Delay
			- Based on propagation and queueing delays for each interface of the routers
	- Each router generates 5 spanning trees and 5 routing tables