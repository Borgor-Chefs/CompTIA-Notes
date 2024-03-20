---
tags:
  - os
  - windows
  - networking
---
# Windows IP Address Configuration

Normally, when connecting to a network, your computer will attempt to reach a [[DHCP|DHCP]] server to obtain an IP address to be used on the network. However, when a DHCP server isn't available or there's an error of some sort, Windows will fall back to [[IP Address Assignment#Self-Assigned|APIPA addressing]] wherein Windows will assign itself an IP in the range of 169.254.0.1 to 169.254.255.254 with a subnet mask of 255.255.0.0.

>Information about this IP address range varies for some reason, not sure why.

When running with this self-assigned IP address, you will not have a connection to the internet, however, you can still communicate with computers in your local network.

## Static IP Addressing

![[Pasted image 20230825160425.png]]

To set a static IP address follow the steps:

1. Open [[Control Panel|Control Panel]]
2. Go to "Network and Sharing Center"
3. Click "Change adapter settings"
4. Right click on the desired adapter (usually this would be Wi-Fi or your wireless adapter)
5. Click "Properties"
6. Find and click "Internet Protocol Version 4 (TCP/IPv4)"
7. Click the "Properties" button

Here you can set a static IP address (if you have one), the subnet, the gateway, along with a DNS server.

## DHCP Failsafe

You should always have multiple DHCP servers installed (or saved somewhere) so that you never have an issue with obtaining an IP address on a network.

However, if your network is fully operational but for whatever reason just doesn't have a DHCP server, then you can bypass APIPA and set a static IP address fallback.

![[Pasted image 20230825160819.png]]

This can be done in the aforementioned static IP address program under the "Alternate Configuration" tab.
