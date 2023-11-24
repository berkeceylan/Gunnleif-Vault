#  CS408 - WEEK2

## Performance Metrics

- **Troughput**
    - Effective capacity of the data bits 
        - reduced by protocol overhead (header + control header)
-  ** Utilization**
    - The ratio of the time that channel is actually used for effective data bits
    - consider 
        - idle time in channel
        - propogation time
        - overheads
        - packet switching delays

----

## Routing

- adaptive routing
    - routing decisons should change as condtions on network change
- routing paths are change when
    - failure of switching node
    - congestion (route around congestion)
- requires exchange of network state information
    - tradeoff: quality of information & overhead

----

## Local Area Networks (LAN)

- Smallar scope than WAN's
    - designed for building or a small campus
- Owned by some organization
- Requires setup and maintance
- Data rates are higher than WAN's
- Traditionally: Broadcast systems
    - tendency to send messages to all devices on the network, regardless of the intended recipient
- Today: LAN -\> wierless LANs

----

## The Internet

- The internet = collection of different networks that run TCP/ IP protocols
    - TCP/IP protocols created in 1974
    - *TCP (Transmission Control Protocol):*
        - Ensures end-to-end communication.
        - Manages data packet assembly before transmission, and reassembly upon receipt.
        - Provides error-checking and ensures data integrity.
    - *IP (Internet Protocol):*
        - Responsible for addressing and routing packets.
        - Ensures data gets sent to the correct destination.
- Evolved from ARPANET (1969)
    - arpanet switch to TCP/IP protocols after 1982-83
- First operational packet switching nework
- Not planned or controlled
- Began Four Locations
    - UCLA
    - University of California at Santa Barbara
    - Universtiy of Utah
    - Stanford Research Institute (SRI)
- Being on internet host machine should 
    - run TCP/IP protocal stack
    - have public/private IP address
        - when packet goes out of the local network 
        - private UP address -\> Public IP address
- **National Science Foundation (NSF)**
    - Until 1986
        - Use of ARPANET avaliable only for ARPA contrators
    - After 1986
        - NSF sponsored extended Internet support
            - NSFNET backbone
        - General research and education community
        - Connceted to ARPANET(both based on TCP/IP)
    - Packet switching networks backbone is NSF in USA
        - NSF policy did noy allow commercial activities
- **Privatization**
    - Until 1995 
        - National governmnets subsidized the internet
    - After 1995
        - Internet subsidization finish in USA
        - Opned to commercial activities
        - Mandated Network Access Points (NAP)
            - designed to serve as neutral exchange points where both commercial and non-commercial networks could interconnect.
            - NAP backbone
- **Applications**
    - *Remote Login*
        - first = telnet and rlogin
            - not secure
        - now = SSH
            - secure
    - *File Transport Protocol(TCP)*
        - transfer of files from one computer to another
        - early ARPANET application
    - *First Killer App: e-mail*
        - In the year 1973, 75% (or three out of every four packets transmitted over the ARPANET) were associated with e-mail communication
- **World Wide Web(WWW)**
    - developep at cern at 1991
    - In 1993 
        - explosive growth
        - emerge of first graphical browser : *Mosaic* 
            - Mosaic -\> Netscape -\> Mozilla -\> Firefox
    - Communication protocol: * HTTP (HyperText Transfer Protocol)*
    - Data stored natively with: *HTML (HyperText Markup Language)*
    - HTTP is the protocol responsible for delivering HTML content (and other web content) from a server to a client (browser)
- **Intranets**
    - Basicly local internet 
        - not intended to be open to global internet
    - Uses TCP/IP
    - Suitable for corporate networks
    - *Pros*
        - can be implemented easily
        - no traning required
        - open architecture
            - add-on applications avaliable

