### Defintion:
- Used to determine which RTO to use for retransmitted segments in [TCP Traffic Control](TCP%20Traffic%20Control.md)
- Answers the some unanswered question in [Jacobson’s Algorithm](Jacobson’s%20Algorithm.md)
- Since timeout is probably due to congestion  -> maintaining the same RTO is not good idea for a retransmitted segment
### Algorithm:
- RTO increases each time a segment is  
- Re-transmitted -> backoff process
	- $RTO_{i+1} = q \times RTO_i$
	- exponential backoff -> RTO for a retransmission is the multiplication of RTO of previous (re)transmission of the same segment and q
- Most commonly q = 2
	- binary exponential backoff