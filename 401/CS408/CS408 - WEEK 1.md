# CS408 - WEEK1

> network is an interconnected or interrelated chain, group or system

## Switching

Main purpose: elaying the data from one node to another until it reaches to destination

WAN = Wide Area Network

### Types Of Switching

#### Circut Switching

- **Pros**
    - Data rate is fixed
        - Smooth process
        - Data send it as one big block
    - Other than propogation delay there is no delay 
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

**Phases of communication(intarnal switching)**

1. Circut establishment
2. Data transfer
3. Circut disconnect

*Each link on path* =\> must reserve enough capacity for connection

*Each node* =\> must have capacity for internal switching and intelegene to work out rooting

**What is internal switching ?**

The process of determining which path to use , establishing that path, maintaning during transfer and disconnecting when transfer ends is called internal switching.

#### Packet Switching

- **Pros**
    - Line efficency
        - No dedicated capacity
    - Data rate conversion
        - each node as own speed
    - Queue System
        - Even network is busy packets can accepted
- **Cons**
    - Not a smooth process (data rate is not fixed)
    - Delay
        - Processing Delay
            - Time it takes for a node to process the packet header
            - More processing needed
        - Variable Delay
            - Due to processing and queuing
        - Transmission Delay
            - Time taken to push all the packet's bits onto the link
            - Link Bandwidth (in bps) / Packet Size (in bits)
        - Propogation Delay
            - Time taken for a signal (or bit) to travel from the sender to the receiver
            - The Length of Channel (Distance) / Propogation Speed
    - Header Overhead: header transfered but dont have the app data

##### **Operation of Packet Switching**

- Data transmited in short blocks (packets)
    - data + header with control info (has destination station adress)
    - store and forward technique: Each node
        -  packet received
        - stored breifly
        - processed (determines next leg of route)
        - passed to next node/ queue to packet to go

##### Datagram Approach

- **Pros**
    - Each packet tread as individually
    - Packets can take practical route
    - Better if few packets
    - More reliable, more flexible
        - In case of node failure, alternative routes can be found
        - routing can be used o avoid congested parts of network
        - *Become idealized more used than Virtual Circut Approach*
- **Cons**
    - Packets may arrive out of order
    - Packets may may go missing 
    - *Receiver is responsible to reorder and retrive missing packets*

##### Virtual Circut Approach

- **Pros**
    - All Packets use the same route
        - Packets are coming same order and they are not lost
    - Rouing decsion is not required (has virtual circut identifier)
    - Faster than datagram
        - Packets are still buffered at switching nodes and qued for output
        -  store, process and forward exist
    - Less flexible, less reliable
        - Loss of a node looses all circuits trought that node (since uses same path)
        - Not a responsive to cognition

![](Switching.png)

#### Total Delay

Total delay is the time needed for data to go from the sender to receiver

Round-tirp Time Delay: total delay + time needed to acknowledment (ACK)

**What is the total delay of N packets and k intermadiate switching node ?** 

- For Packet Switching: 
    - Transmission Time: (N+k) x Ttrans
    - Propogation Time: (k+1) x Tprop
    - Processing Time: k x tproc
    - Total : (N+k) x Ttrans + (k+1) x Tprop +  k x tproc
- For Circut Switching:
    - Total : Ttrans + (k+1) x Tprop
    - No processing delay exist

