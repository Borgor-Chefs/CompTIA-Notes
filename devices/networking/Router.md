---
tags:
  - device
  - networking
---
# Routers

![[Pasted image 20230322195731.png]]

This piece of hardware routes packets from one network to another based on the source and destination IP address. When a data packet is received, the router will inspect the packet and determine if the packet was meant for its network or another network.

![[Pasted image 20230322200039.png]]

If the router determines that the data packet is meant for its network then it will receive it and pass it along to the proper device, if not it will send the packet off to another network. This is essentially the gateway for the network.

In the above example, the router will only accept data packets colored red since this is traffic meant for this network. If not, the router will pass the data along to other networks. Keep in mind, this is a very simplified example.

## Service Set Identifier (SSID)

![[Pasted image 20230421171706.png]]

This is the name of a network you can connect to via. a [[Router|router]].
It is shared amongst all devices in the network.

The image above is an example of how computers scan for wireless networks.

## Channel

This delves into the radio/FM communication side of things. If you are experiencing interference or picking up junk data it might be because there is another router in the near vicinity which is broadcasting on the same channel and same frequency.

To fix this, simply change the channel the router operates on (within the router's control panel).

## Security

You can set the security mode that the device uses, e.g., WPA2-Personal or WPA3-Enterprise.

>See [[Wireless Security Modes]] for more.

## SOHO Routers

SOHO stands for "Small Office / Home Office" [[Router|router]] and these are primarily by homes and small businesses.

To access the configuration of this router, type in the IP address of the router in your browser and login to the router.

From there you can access settings such as the [[IP Address#Private IP Address|private IP address]], [[#Service Set Identifier (SSID)|SSID]], [[DHCP|DHCP]] server, etc.
