### Definition:
- Used to determine which round-trip time to use as input to [Jacobson’s Algorithm](Jacobson’s%20Algorithm.md) if a segment is retransmitted in [TCP Traffic Control](TCP%20Traffic%20Control.md)
- If a segment is retransmitted, the ACK arriving may be:
	- For the first copy of the segment?
	- For the second copy?
- TCP source cannot distinguish between these two cases
- wrong assumptions may yield wrong results and estimates
### Algorithm:
- Do not measure RTT for retransmitted segments to update SRTT and SDEV
- Calculate backoff RTO when re-transmission occurs
- Use backoff RTO until ACK arrives for segment that has not been re-transmitted
- When ACK is received for an un-retransmitted segment
	- for a segment sent and its ack is received without retransmission
	- Jacobson algorithm resumes to calculate future RTO values