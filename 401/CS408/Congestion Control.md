### Definition:
- We have 2 important performance metrics:
	- Throughput
	- Delays
		- Transmission delay -> Time for transmitter to send all bits of packet
		- Propagation delay -> Time for one bit to transit from source to destination
		- Processing delay ->Time required to process packet at source prior to sending
		- Queuing delay: Time spent while waiting in queues
### Queuing Delay:
- Grow dramatically as system approaches to capacity
- In shared facilities (e.g., network, transmission line, road network, checkout lines, ...)
	- Performance typically worsens exponentially as the demand approaches to the capacity
	- when we get closer to capacity we should be very conservative since it grows exponentially.
- **Queuing Theory:**
	- $\lambda$ = mean arrival rate (packet/sec)
	- $\mu$ = mean processing rate (packet/sec) = $1/T_s$
	- $\rho$ = $\lambda / \mu$ = utilization
		- $\rho <1$ = stable
		- $\rho \geq 1$ = unstable -> queue grow to infinity
	- **M/M/1 Queues:**
		- First M -> Poisson arrival
		- Second M -> Service Time (Expo. distribution.)
		- 1 -> number of queue
		- $\lambda \sqsupset \sqsupset \sqsupset \sqsupset \sqsupset \sqsupset \gg \mu$ 
		- r = mean number of items waiting in the queue = $\rho / 1- \rho$
		- $T_w$= avg. waiting time in the queue = $r\times T_s = \rho/1-\rho \times 1/\mu$ 
### Congestion:
- Data network is a network of queues
- Congestion occurs when the number of packets being transmitted through the network approaches the packet handling capacity of the network
	- If the arrival rate > transmission rate -> queues grow to infinity -> unresolvable congestion
	- If the arrival rate < transmission rate
		- Until % 80 utilization it is okay but we need to be careful while getting close the capacity
		- Generally 80% utilization is critical
		- growth in queue = more delay
		- queues may overflow since it is of finite capacity
- So congestion can occur and create some problems so wee need to control it.
### Congestion Control:
- Aims to keep the number of packets below the %80 utilization
- If packets
	- arrive too fast to be processed/routed -> input buffers will fill up
	- arrive faster than that can be transmitted -> output buffers will fill up
- **Precautions:**
	- Discard packets ->packets are lost not good
	- Flow control over neighbors -> Inform the neighbours about congestion control flow.
- **Methods:**
	- **Backpressure:**
		- If node becomes congested
			- it can slow down or halt flow of packets from its neighbors
		- That may cause longer queues at neighbors and they do the same
		- Propagates back to source
		- Used in connection oriented networks that allow hop by hop flow control 
			- e.g. X.25 – old style network layer
			- not for TCP/IP
	- **Choke Packet:**
		- Control packet
			- Generated at congested node
			- Sent to source node
			- e.g. [ICMP](ICMP.md) source quench
				- From router or from destination
				- Source cuts back until no more source quench messages
				- Sent for every discarded packet, or when congestion is anticipated
		- Not a sophisticated method, but applicable for [IP](IP.md)
	- **Implicit Congestion Signaling:**
		- With congestion
			- Delay may increase
			- Packets may not be acknowledged during timeout period
		- Source can detect these as implicit indications of congestion and reduces the flow
			- Intermediate systems do not need to take any action
		- Useful on connectionless (datagram) network -> e.g. IP based
		- In TCP/IP, logical connection is established at TCP level
			- TCP has acknowledgment and flow control mechanisms that help implicit congestion signalling
	- **Explicit Congestion Signaling:**
		- Network alerts end systems of increasing congestion
		- End systems take actions to reduce the load
		- Backward
			- notifies the source about congestion
		- Forward
			- notifies the destination about congestion
		- Notification information is added to data packets
### Issues:
- **Fairness:**
	- discarding the last received packet is not fair
	- A fair approach: 
		- multiple queues for multiple source-destination socket pairs 
		- all equal length
- **Quality of service:**
	- different priorities for different connection types 
		- voice, video, email, network management
	- Some types of traffic are less important than the others in the case of congestion
- **Reservations:**
	- congestion avoidance mechanism
	- traffic contract between user and network
	- network makes necessary reservations to keep its promise
	- user tries not to overuse the reserved capacity
		- Traffic policing: compares the actual traffic with the one in contract
	- Integral part of RSVP protocol of IP-based internets