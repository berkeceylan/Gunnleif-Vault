### Definition:
- Used to determine RTO in [TCP Traffic Control](TCP%20Traffic%20Control.md)
- Estimate the variance of RTT and then decides RTO
- Standard method
	- RTT may show high variance
		- Variance in packet size may cause variance in transmission delays
		- Network traffic load may change abruptly due to other sources
		- Peer may not acknowledge segments immediately
### Algorithm:
- $SRTT(K + 1) = (1 – g) \times SRTT(K) + g \times RTT(K + 1)$
	- estimated RTT for K+2 nd segment
- $SERR(K + 1) = RTT(K + 1) – SRTT(K)$
- $SDEV(K + 1) = (1 – h) \times SDEV(K) + h \times |SERR(K + 1)|$
	- standard deviation that will be used for the timeout value for K+2 nd segment
- $RTO(K + 1) = SRTT(K + 1) + f \times SDEV(K + 1)$
	- timeout value (RTO) for K+2 nd segment
- Based on experiments
	- g = 0.125 
	- h = 0.25
	- f= 2  or  f = 4 -> 4 is widely used
- **The behavior of RTO:**
	- RTO is quite conservative while RTT is changing
	- Then begins to converge
### Other Factors:
- Jacobson’s algorithm is a good method for determining RTO
- However:
	- What RTO to use for retransmitted segments?
		- ANSWER: [Exponential RTO Backoff Algorithm](Exponential%20RTO%20Backoff%20Algorithm.md)
	- Which round-trip time to use as input to Jacobson’s algorithm if a segment is retransmitted?
		- ANSWER: [Karn’s Algorithm](Karn’s%20Algorithm.md)