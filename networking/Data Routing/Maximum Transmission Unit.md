---
tags:
  - networking
  - osi
  - routing
---
# Maximum Transmission Unit (MTU)

![[Pasted image 20240312151206.png]]

>Above is an example of the fragment information in the [[OSI Model#Data Link Layer|IP header]] of a packet.

This is the maximum IP packet size to transmit and to not [[#IP Fragmentation|fragment]] into other packets. The reason why this is important is because this slows down the network because instead of one packet being sent, you're sending multiple.

What's worse is if you accidentally lose a fragmented packet.

However, it's difficult to know what the MTU is along the path because it depends on how many hops it takes for you to get to the destination, but you can try and [[#Troubleshooting the MTU|troubleshoot]] it.

## IP Fragmentation

![[Pasted image 20240312151447.png]]

This is an example of fragmented packets, where the maximum size to send over the network is 16 bytes.

## Troubleshooting the MTU

>Apparently, MTU sizes are usually configured once when the network infrastructure is built and rarely change after that.

A significant concern is for tunneled traffic, i.e., using a VPN. Because the MTU for your VPN might be smaller than your local ethernet segment.

If you send packets with the "Don't Fragment" (DF) bit set, it might work and it might not. If it doesn't work, your [[Router]] *should* send an ICMP message back to you, saying that the packet is too big and needs to be fragmented.

You can test the MTU of your network using the following commands:

- On [[!Windows|Windows]], `ping -f -l 1472 8.8.8.8`
- On [[!Linux|Linux]] and [[!Apple|macOS]], `ping -D -s 1472 8.8.8.8`

>The reason why it's 1472 bytes is because that's (usually) the maximum size minus all the other header information. I.e., 1500 bytes - 8 byte ICMP header - 20 bytes IP header = 1472.
