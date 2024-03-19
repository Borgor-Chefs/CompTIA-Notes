# Transceivers

![[Pasted image 20240319165012.png]]

>The above images shows a [[Switch]] with two transceiver ports. The device in the left hand transceiver port is a [[Fiber Optic Cables#Local/Lucent Connector (LC)|LC]] connector.

This is a device that has a transmitter and a receiver (usually) built into a single component. This is also something that's modular and are made for both [[Digital Cables|copper]] and [[Fiber Optic Cables|fiber]] connections.

Network transceivers vary in how they transmit data and how many connections and speeds they support:

- [[#Methods of Data Transmission of Transceivers]]
    - [[#Duplex Transceivers]]
    - [[#Bi-Directional (BiDi) Transceivers]]
- [[#Transceiver Form Factors]]
    - [[#Small Form-factor Pluggable (SFP)]]
    - [[#Enhanced Small Form-factor Pluggable (SFP+)]]
    - [[#Quad Small Form-factor Pluggable (QSFP)]]
    - [[#Enhanced Quad Small Form-factor Pluggable (QSFP+)]]

## Methods of Data Transmission of Transceivers

There are two ways transceivers can send data over their connections:

- [[#Duplex Transceivers]]
- [[#Bi-Directional (BiDi) Transceivers]]

### Duplex Transceivers

![[Pasted image 20240319165330.png]]

This type of connection between transceivers uses two physical cables to send and receive data. One transceiver's transmit line (TX) sends information to the other's receive line (RX) and vice versa.

### Bi-Directional (BiDi) Transceivers

![[Pasted image 20240319165445.png]]

This type of connection uses two different **wave lengths** to transmit data on a single fiber connection. This reduces the number of fiber runs by half.

## Transceiver Form Factors

![[Pasted image 20240319170958.png]]

>Here's the size comparison between [[#Small Form-factor Pluggable (SFP)|SFP]] and [[#Quad Small Form-factor Pluggable (QSFP)|QSFP]] network transceivers.

There are multiple form factors for network transceivers, being:

- [[#Small Form-factor Pluggable (SFP)]]
- [[#Enhanced Small Form-factor Pluggable (SFP+)]]
- [[#Quad Small Form-factor Pluggable (QSFP)]]
- [[#Enhanced Quad Small Form-factor Pluggable (QSFP+)]]

Mind you, these can be combined with the [[#Methods of Data Transmission of Transceivers|duplex and bi-directional]] variants to product things like a BiDi QSFP. The reason why you would want this is to save on efficiency and number of possible fiber connections.

### Small Form-factor Pluggable (SFP)

This is commonly used to provide 1Gbit/s fiber connections, there are also 1Gbit/s [[Digital Cables#Register Jack 45 (RJ-45)|RJ-45]] SFPs available.

### Enhanced Small Form-factor Pluggable (SFP+)

This is the exact same physical size as regular [[#Small Form-factor Pluggable (SFP)|SFPs]] but are enhanced to increase the throughput, specifically up to speeds of 16Gbit/s.

This is common with [[Cable Categories|10 gigabit Ethernet]].

### Quad Small Form-factor Pluggable (QSFP)

This is similar to an [[#Small Form-factor Pluggable (SFP)|SFP]], but it is physically bigger and has 4 channels, meaning 4 connections. This provides 4 Gbit/s connections.

### Enhanced Quad Small Form-factor Pluggable (QSFP+)

Similar to the [[#Quad Small Form-factor Pluggable (QSFP)|QSFP]], but this has 4 [[#Enhanced Small Form-factor Pluggable (SFP+)|SFP+]] connections. This provides 40 Gbit/s connections.
