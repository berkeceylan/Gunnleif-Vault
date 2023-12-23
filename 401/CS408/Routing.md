## Routing

- Adaptive routing
    - routing decisions should change as conditions on network change
- Routing paths are change when
    - failure of [Switching](Switching.md) node
    - congestion (route around congestion)
- requires exchange of network state information
    - tradeoff: quality of information & overhead

--------note dump----------
- End systems and routers maintain routing tables
	- Indicate next router to which datagram should be sent
	- Static
		- Tables do not change but may contain alternative routes
	- Dynamic
		- if needed, the tables are dynamically updated
		- Flexible response to congestion and errors
		- status reports issued by neighbors about down routers
- Source routing
	- Source specifies route as sequential list of routers to be followed
	- useful, for example, if the data is top secret and should follow a set of trusted routers.
- Route recording
	- routers add their address to datagrams
	- good for tracing and debugging purposes