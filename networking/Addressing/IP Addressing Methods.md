Tags: [#networking]

# IP Addressing Methods

There are two ways that a computer can be assigned an [[IP Address|IP address]]:

- dynamically
- statically
- self-assigned (APIPA)

## Dynamic IPs

A computer will search for a [[DHCP|DHCP]] (dynamic host configuration protocol) server and request an [[IP Address|IP address]], the DHCP server will assign an IP address to that computer along with:

- a subnet mask
- a default gateway
- a DNS server

This is "the best choice" because it makes managing a network a lot easier. However, you could run into issues if you rely on devices having the same [[IP Address|IP address]] each time they connect to the network.

## Static IPs

![[Pasted image 20230331165556.png]]

This is where the user manually sets the [[IP Address|IP address]], [[IP Address#Subnet (Mask)|subnet]], default gateway and sometimes the DNS server of a computer.

## Self-Assigned

![[Pasted image 20230331165933.png]]

For computers running Windows 98 or later versions of Windows, in the event that a [[DHCP|DHCP]] server isn't available, the computer will assign an [[IP Address|IP address]] to itself on the 169.254.0.0 network so that it can communicate with computers on this same network. This kind of addressing is called "Automatic Private IP Address Assignment" or APIPA.

When a [[DHCP|DHCP]] server becomes available, the computer will request an IP from that server and replace the 169.254.0.0 with one from the server.
