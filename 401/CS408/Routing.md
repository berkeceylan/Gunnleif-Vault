## Routing In IP
### Definition:
- Process of directing data packets from a source to a destination in an [IP](IP.md) network
- Uses  [Routers](Routers.md) to forward data
- To make packet forwarding decisions **Routing Tables** are used
- Determines the best path based on network topology and protocols
- Putting data to network = cost
- Getting data from network = no cost
- Uses mostly adaptive routing 
### Types: 
- **Fixed Routing:**
	- Single permanent route configured for each source-destination pair
	- Routes are fixed
	- May change when topology changes (not so often)
		- Mostly manual
		- No dynamic updates
- **Adaptive Routing:**
	- As conditions on internetwork change, routes may change
	- Flexible response to congestion and failure
		- Failure of networks or networks
		- Congestion -> not use heavily used route
	- **Classification:**
		- Based on information sources
		- **Local:**
			- route each datagram to network with shortest queue
			- Balance loads on outgoing networks
			- May not be heading in correct direction
			- Rarely used
		- **Adjacent Nodes:**
			- Delay and outage info from adjacent nodes
			- Distance vector algorithms
		- **All Nodes:**
			- Link-state algorithms
	- **Challenges:**
		- Overhead Increase:
			- Complex routing decisions -> Router processing overhead increases
			- Routers depends on information collected in another placed
				- routing decision quality increase (good)
				- overhead increases (bad)
		- Unpredicted react period:
			- May React Too Fast:
				- Can lead to congestion due to oscillation or "fluttering" in the network.
			- May React Too Slow:
				- Routing decisions might become outdated as network conditions change rapidly.
		- Looping
			- Packet mistakenly returns to the same router
			- Occurs when connectivity changes are not promptly shared among routers
			- Routing algorithms must actively avoid looping to ensure efficiency
			- Not a common case
### Routing Table:
- **Definition:**
	- One routing table is needed for each router
	- One entry for each destination network 
		- Not for each destination host
		- when datagram reached to network router can pass it to host 
	- Each entry shows next node on the route to destination
		- Entire route is not comprehended
	- Host may also have routing tables if multiple routers attached to network
	- Host do not need routing table if network has single router (gateway)
- **Types:**
	- Static
		- Tables do not change but may contain alternative routes
	- Dynamic
		- if needed, the tables are dynamically updated
		- Flexible response to congestion and errors
		- status reports issued by neighbors about down routers
### Methods:
#### Distance-Vector Routing Method:
- Suitable for [Interior Routing Protocols (IRP)](Interior%20Routing%20Protocols%20(IRP).md)
	- require homogenous metrics
	- require flooding the link state information
- Routers share data with directly connected neighbors
	- Nodes are neighbors if directly connected or on the same network
- Routing Table:
	- Each node maintains a table with;
		- distance vectors
		- next-hop vectors for each destination
	- Tables includes one entry per destination network
	- Tables includes link cost vectors for directly attached networks
- Routers transmit distance vectors with path costs to all neighbors.
	- Changes in routing information can take a while to spread through the network.
- First-generation algorithm in ARPANET
- [RIP (Routing Information Protocol)](Interior%20Routing%20Protocols%20(IRP).md#RIP%20(Routing%20Information%20Protocol)) uses this method
#### Link-State Routing Method:
 - Suitable for [Interior Routing Protocols (IRP)](Interior%20Routing%20Protocols%20(IRP).md)
	 - require homogenous metrics
	 - require flooding the link state information
- Created as an improvement over the distance-vector method
- Each router assesses the cost of its links upon initialization
- Routers broadcast their link costs to the entire network, not just to neighbors.
- Routers monitor and advertise significant changes in link costs.
	- Allows routers to have a complete view of the network's topology
	- Routers can calculate the shortest path to each destination (Dijkstra)
- Each router creates a routing table indicating the first hop towards each destination
- Second generation routing algorithm for ARPANET
- [OSPF (Open Shortest Path First)](Interior%20Routing%20Protocols%20(IRP).md#OSPF%20(Open%20Shortest%20Path%20First)) uses this method
#### Path-Vector Method:
- Suitable for [Exterior Routing Protocols (ERP)](Exterior%20Routing%20Protocols%20(ERP).md)
- Provide information about which networks can be reached by a given router and Autonomous Systems crossed to get there
	- Does not include distance or cost estimate
- [Border Gateway Protocol (BGP)](Exterior%20Routing%20Protocols%20(ERP).md#Border%20Gateway%20Protocol%20(BGP)) uses this method




