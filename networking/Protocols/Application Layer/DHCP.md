---
tags:
  - networking
  - application_layer
  - osi
---
# Dynamic Host Configuration Protocol (DHCP)

>[[Networking Ports|Standard port]]: 67/68
>[Link](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

This is used to assign IP addresses to computers along with manage them. This is essentially a broker for IP addresses for computers that dynamically obtain their IP.

## DHCP Server was removed from the network

![[Pasted image 20230331171012.png]]

If a DHCP server disappears from the network and the computer's IP expires and it asks for a new one, it will fail and this computer will be unable to communicate on the network until the DHCP server is back online or you manually set its IP.

## Adding a DHCP server to the network

![[Pasted image 20230331170956.png]]

If you add a second DHCP server to the network it must be configured properly else it could assign a computer the same IP address as another computer, screwing up the network. You must configure the address pool correctly.
