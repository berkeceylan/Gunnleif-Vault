## Circuit Switching
### Definition:
- A type of [Switching](Switching.md) in WANs
- Dedicated communication path between two stations
	- Connected sequence of links between nodes
	- each link on the path -> must reserve enough capacity for the connection
	- each node -> must have capacity for internal switching and intelligence to work out rooting
- **Internal Switching:**
	- The process of determining which path to use , establishing that path, maintaining during transfer and disconnecting when transfer ends is called internal switching
	- **Phases of communication:**
		1. Circuit establishment
		2. Data transfer
		3. Circuit disconnect
- Example : Telephone Network
## Total Delay:
- Total delay: time needed for data to go from the sender to receiver
- Round Trip  Time Delay(RTT): total delay + time needed to acknowledgment (ACK)
- Assume: N packets and k intermediate switching node
	- Total : Ttrans + (k+1) x Tprop
	- No processing delay exist
### Pros & Cons:
- **Pros**
    - Data rate is fixed
        - Smooth process
        - Data send it as one big block
    - Other than propagation delay there is no delay 
        - transmission delay also exist in total but it is very little
    - Best for voice communication 
        - Telephone Network
- **Cons**
    - Delay before transfer to establish channel
    - Capacity dedicated for duration of connection even data is not transfered
        - Low utilization 
        - Not good for data transfer
            - Reason 1: Path will be mostly idle 
            - Reason 2: Data rate is fixed (Limits the utility of  high-speed stations)



