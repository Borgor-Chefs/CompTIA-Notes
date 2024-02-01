---
tags:
  - networking
  - protocol
  - encryption
  - security
---
# Wireless Security Modes

There are various wireless methods to choose from and here's what they do:

- [[#Open System|open system]]
- [[WEP]]
- [[#WPAX-Personal|WPA/WPA2-Personal]]
- [[#WPAX-Enterprise|WPA/WPA2-Enterprise]]
- [[#WPAX-Personal|WPA2-Personal]]
- [[#WPAX-Enterprise|WPA2-Enterprise]]
- [[#WPAX-Personal|WPA2/WPA3-Personal]]
- [[#WPAX-Enterprise|WPA2/WPA3-Enterprise]]
- [[#Wi-Fi Protected Setup (WPS)]]
- [[#MAC Filter|MAC Filtering]]
- [[#Demilitarized Zone (DMZ)]]

>Note that the X in WPAX stands for the type of [[WPA]] standard.

## Open System

No authentication required.

## WPAX-Personal

Basically, everyone uses a pre-shared key (PSK) to authenticate.

## WPAX-Enterprise

Users authenticate individually using an authentication server (i.e., [[RADIUS]]).

## Wi-Fi Protected Setup (WPS)

![[Pasted image 20230421173109.png]]

>Above is an example of a WPS configuration page.

This protocol was designed for people that don't have a good nor any understanding of wireless networks so that they can easily join a protected network without having to worry about configuring anything important nor hard.

## MAC Filter

![[Pasted image 20230421173337.png]]

This is just a white/black list for MAC addresses which determines if a device with said MAC address is allowed to connect to the network or not. Really simple.

## Demilitarized Zone (DMZ)

![[Pasted image 20230421173704.png]]

This fully exposes a computer to the internet by forwarding all its ports. This is useful for when you're troubleshooting a [[Firewall|firewall]] issue.

A computer in the DMZ **must** be assigned a [[IP Addressing Methods#Static IPs|static IP address]] and not one assigned dynamically via. a [[DHCP]] server.
