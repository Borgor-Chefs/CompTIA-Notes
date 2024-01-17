---
tags:
  - os
  - windows
  - networking
---
# Windows Network Connections

![[Pasted image 20230825162038.png]]

In [[Control Panel|Control Panel]], you can manually create new network connections via. a wizard. You have a couple options:

- a connection to the internet
- [[#Network Connection|a connection to a network]]
- [[#Workplace Connection|a connection to a workplace]] (basically a VPN connection)

You can also view ethernet connections.

>Windows also "supports" WWAN (Wireless Wide Area Network) options (e.g., connect to a cellular network) but this is third-party software and hardware.

## Network Connection

![[Pasted image 20230825162057.png]]

Here you enter:

- the name (SSID) of the network
- the security type of the network
- the encryption type of the network
- an optional security key

Along with:

- start this connection automatically (helpful if this is your default home network)
- connect even if the network is not broadcasting

## Workplace Connection

>This type of connection also supports a dial-up option.

![[Pasted image 20230825162118.png]]

This is most likely a VPN connection, because it's not guaranteed that the origin from where you're connecting doesn't have some type of packet sniffer or is actually a proper network and not a man in the middle attack. Therefore, (smarter) workplaces will have a VPN concentrator, which is a public facing piece of hardware to connect to.

This VPN concentrator validates upon connection that you, the connecter, should actually be connecting to this server, which if true, it will establish an encrypted tunnel for you to send information through, free from any prying eyes (however this fails if your handshake gets caught and broken).

Here you can set:

- the internet address (a hostname or a proper IP address)
- a destination name (just a descriptor for humans)

You can also:

- use a smart card (this is like 2FA for VPNs)
	- this could be: something you know, have or are
- remember my credentials (so you don't have to log in every time you connect)
- allow other people to use this connection
	- I assume that this is like a [[Windows Network Technologies#Shared Resources|network share]] to other computers on your network
