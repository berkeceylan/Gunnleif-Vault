## Performance Metrics

### Throughput
- Effective capacity of the data bits 
	- reduced by protocol overhead (header + control header)
	- Utilization x  channel rate
### Utilization
- The ratio of the time that channel is actually used for effective data bits
- Consider 
	- idle time in channel
	- propagation time
	- overheads
	- packet switching delays
### Delays in [Switching](Switching.md):
- Round Trip  Time Delay (RTT): total delay + time needed to acknowledgment (ACK)
- Transmission time (delay)
	- Time taken to emit all bits into medium
	- Packet Size (in bits) / Link Bandwidth (in bps) 
- Propagation time (delay)
	- Time for a bit to traverse the link
	-  The Length of Channel (Distance) / Propagation Speed
- Processing time (delay)
	- time spent at the recipient or intermediate node for processing
- Queuing time (delay)
	- waiting time at the queue to be sent out
![](Attachments/Delay.png)
