### Defintion:
- A collision resolution algorithm used in [Ethernet](Ethernet.md)
- Low delay -> small amount of waiting stations
- Large delay -> large amount of waiting stations
### Operation:
- Random waiting period but consecutive collisions increase the mean (i.e. average) waiting time
	- mean waiting time doubles in the first 10 retransmission attempts
	- after first collision -> waits 0 or 1 slot time (selected at random)
	- if collided again (second time) -> waits 0, 1, 2 or 3 slots (at random)
	- if collided for the ith time -> waits 0, 1, …, or 2i-1 slots (at random)
- The randomization interval is fixed to 0 … 1023 after 10th collision
- Station tries a total of 16 times and then gives up if cannot transmit
