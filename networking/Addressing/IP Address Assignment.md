---
tags:
  - networking
---
# IP Addressing Methods

There are three ways that a computer can be assigned an [[IP Address|IP address]]:

- [[#Dynamic IPs]]
- [[#Static IPs]]
- [[#Automatic Private IP Address (APIPA)]]

## Dynamic IPs

A computer will search for a [[DHCP|DHCP]] (dynamic host configuration protocol) server and request an [[IP Address|IP address]], the DHCP server will assign an IP address to that computer along with:

- a [[IP Address#Subnet (Mask)|subnet mask]]
- a [[IP Address#Gateway IP Address|default gateway]]
- a [[DNS|DNS server]]

This is "the best choice" because it makes managing a network a lot easier. However, you could run into issues if you rely on devices having the same [[IP Address|IP address]] each time they connect to the network.

## Static IPs

![[Pasted image 20230331165556.png]]

This is where the user manually sets the [[IP Address|IP address]], [[IP Address#Subnet (Mask)|subnet]], [[IP Address#Gateway IP Address|default gateway]] and sometimes the [[DNS]] server of a computer.

## Automatic Private IP Address (APIPA)

![[Pasted image 20230331165933.png]]

>Might also be referred to as "self-assigned".

For computers running [[!Windows|Windows 98]] or later versions of Windows, in the event that a [[DHCP|DHCP]] server isn't available, the computer will assign an [[IP Address|IP address]] to itself on the 169.254.0.1 network so that it can communicate with computers on this same network.

When a [[DHCP|DHCP]] server becomes available, the computer will request an IP from that server and replace the APIPA address with one from the server.

>A computer will pick a random [[IP Address]] from the APIPA range and broadcast an [[ARP]] message to the network to confirm that this address isn't in use. If no computer on the network is using that address, then the computer will take it.
