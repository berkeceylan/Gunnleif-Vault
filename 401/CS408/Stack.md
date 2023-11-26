# Physical Layer Overview
- The physical layer is responsible for the transmission of raw bit streams over a physical medium.

## Data Transmission
- Converts digital data into Electromagnetic (EM) signals for transmission through various media.

## Transmission Medium
- [[Guided Media]]: Includes [[Twisted Pair]], [[Optical Fiber]], and [[Coaxial Cable]].
- [[Unguided Media]]: Uses air or water to transmit signals without a physical guide.

## Spectrum & Bandwidth
- Spectrum refers to the range of frequencies contained in a signal.
- Bandwidth is the width of the spectrum and directly relates to data rate and potential transmission speed.

## Data Rate and Bandwidth
- The relationship between data rate and bandwidth is governed by the signal's spectrum.
- Higher bandwidth usually allows for a higher data rate and less distortion but can be more expensive.

## Transmission Media Types
### Guided Media
- Twisted pair cables: Used for telephone networks and Ethernet.
- Optical fibers: Provide high data rates and are used in long-distance communication lines and LANs.
- Coaxial cables: Versatile and used for TV distribution, internet, and long-distance telephone transmission.

### Unguided Media
- Radio, microwave, and infrared transmissions are common forms of unguided media.
- Microwave frequencies are highly directional and require line-of-sight, often used in satellite communications.

## Transmission Characteristics
### Twisted Pair
- Pros: Cheap and easy to work with, with categories ranging from Cat 3 to Cat 8 for varying data rates.
- Cons: Short range and susceptible to EM interference.

### Coaxial Cable
- Less vulnerable to interference, but requires periodic amplifiers.

### Optical Fiber
- Offers great capacity and low attenuation, with no EM interference, making it secure and reliable for various applications.

### Wireless Transmission
- Includes directional and omnidirectional transmission methods, with frequencies ranging from 1GHz to 40GHz for microwave and 30MHz to 1GHz for broadcast radio.

## Synchronization in Transmission
### Asynchronous Transmission
- Transmits data one character at a time with no need for a common clock signal.
- Overhead includes start, stop, and parity bits for each character.

### Synchronous Transmission
- Transmits blocks of data with a common clock signal, reducing overhead except for error detection/correction codes.

# Backlinks to Related Topics
- [[DNS]]
- [[TCP/IP]]
- [[Socket]]
