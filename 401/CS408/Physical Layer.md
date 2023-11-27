### Definition:
- Responsible for the transmission of raw bit streams over a physical medium
- First and lowest layer in both the [OSI](OSI) model and the [TCP/IP](TCP/IP) protocol stack
### Properties:
- Defines hardware specifications like cables, cards, and physical aspects.
- Handles the bit-level transmission.
- Governs the encoding and signaling schemes.
- Manages data transmission rates.
- Deals with network topology and design.
### Spectrum and Bandwith:
- **Spectrum**:
	- Range of frequencies the physical layer can transmit
- **Bandwith**:
	- Difference between the highest and lowest frequencies of the channel
		- i.e. width of the spectrum
		- Expressed in Hertz (Hz)
	- Higher bandwidth -> higher data rate
		- more data can be transmitted in higher speed
	- Less distortions -> higher bandwidth
		- expensive
	- More distortions -> less bandwidth
		- cheap
	- Infinite bandwidth can be achieved by perfect square however this is not possible in real life
### Data Transmission 
- Converts digital data into Electromagnetic (EM) signals for transmission through various media.
- There are two types of [medium in data transmission](https://www.geeksforgeeks.org/types-transmission-media/)
	- **[Guided Media](Guided%20Media.md)**:
		- **[Twisted Pair](Twisted%20Pair.md)**: 
			- Common in local area networks and telephone systems.
		- **[Coaxial Cable](Coaxial%20Cable.md)**:
			- Used for television distribution and internet access.
		- **[Optical Fiber](Optical%20Fiber.md)**: 
			- Offers high data rates and is used in long-haul network connections.
	- **[Unguided Media](Unguided%20Media.md)**:
		- **[](Unguided%20Media.md#Wireless%20Transmission%20|Wireless%20Transmission)**: 
			- Radio, microwave, and infrared are primary forms.
## Synchronization
- Problem: sender and receiver should be synchronized at the bit level.
	- Sender and receiver 
		- must cooperate
		- must know when to start and stop sampling
		- must know the rate of data
- There are two types of solution: A good [comparison](https://www.geeksforgeeks.org/difference-between-synchronous-and-asynchronous-transmission/) of types
	- [Asynchronous Transmission](Asynchronous%20Transmission.md): 
		- Data is sent one character at a time with start and stop bits.
	- [Synchronous Transmission](Synchronous%20Transmission.md): 
		- A continuous stream of data is sent with timing information.


