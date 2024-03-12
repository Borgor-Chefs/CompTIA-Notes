---
tags:
  - networking
---
# Network Topologies

Network topologies are ways to organize devices on a network and how devices connect to other devices and what hops they have to go through in order to do so.

They are:

- [[#Star Network]]
- [[#Ring Network]]
- [[#Bus Network]]
- [[#Mesh Network]]
- [[#Hybrid Topologies]]
- [[#Wireless Network Topology|Wireless Networks]]

>Some networks aren't explicitly wireless nor wired but are more just types of networks based on the devices' configuration.
>- [[#Bus Network|bus networks]] are explicitly wired
>- [[#Wireless Network Topology|wireless networks]] are explicitly wireless (no shit)

## Star Network

![[Pasted image 20240312153059.png]]

This is called the "star" or "hub and spoke" topology because of its looks. This is most commonly used across all [[Network Types|types of networks]]. Where all devices are connected to a central device.

## Ring Network

![[Pasted image 20240312153208.png]]

This is really no longer used in more local networks but is still used in many [[Network Types#Metropolitan Area Network (MAN)|MANs]] and [[Network Types#Wide Area Network (WAN)|WANs]]. This isn't for speed but for redundancy. If one of the connections in this ring is severed, the flow of traffic can simply flow in the other direction to reach its destination.

## Bus Network

![[Pasted image 20240312153621.png]]

This is an earlier form of network structure where there was a single [[Coaxial Cables|coaxial cable]] connecting all of the devices together. This is a simple network but is prone to errors, if there was a break at any part of the connection, it would disable/break the entire network.

The only place that you would see this type of network nowadays is in your car, it is called a "Connector Area Network" (CAN bus). This network connects all of your car's sensors together.

## Mesh Network

![[Pasted image 20240312153912.png]]

This is most commonly found and used in [[Network Types#Wide Area Network (WAN)|WANs]], to provide redundancy, fault-tolerance or load balancing. This is also good for fully connected or partially connected networks.

## Hybrid Topologies

![[Pasted image 20240312154145.png]]

>The above image shows multiple [[#Star Network|star networks]] being connected by a single [[#Ring Network]].

This is just a combination of multiple physical network topologies. Most networks are hybrid.

## Wireless Network Topology

In a wireless network, all connected devices communicate wirelessly (no shit) and through an access point.

However, you don't necessarily need a wireless access point to form a wireless network. You can create an ad hoc network with no infrastructure and have these devices communicate amongst themselves.

You can form a wireless mesh network from ad hoc devices that work together to form a mesh "cloud" network which can self form and self heal whenever a device powers off.

IoT devices can form a mesh network to communicate.
