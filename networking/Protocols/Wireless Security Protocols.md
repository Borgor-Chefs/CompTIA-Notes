---
tags:
  - networking
---

# Wireless Security Protocols

These are protocols for authenticating to a router/wireless access point (WAP) from your device along with encrypting traffic going to and from the WAP.

Here are the most common methods:

- [[#Wired Equivalent Privacy (WEP)|WEP]]
- [[#Wi-Fi Protected Access (WPA)|WPA]]
	- [[#WPA2|WPA2]]
- [[#Wi-Fi Protected Setup (WPS)|WPS]]
- [[#MAC Filter|MAC Filter]]
- [[#Demilitarized Zone (DMZ)|DMZ]]
- [[#Port Forwarding|Port Forwarding]]

## Wired Equivalent Privacy (WEP)

![[Pasted image 20230421172353.png]]

This is a security protocol which aimed to provide encryption for wireless devices on a network.
Turns out, this protocol was flawed because the 40-bit encryption key was **easily hackable**.

## Wi-Fi Protected Access (WPA)

This protocol was designed to succeed and fix all the problems that [[#Wired Equivalent Privacy (WEP)|WEP]] had. This uses a stronger encryption method using [[TKIP|TKIP]] (temporal key integrity protocol).

[[TKIP|TKIP]] dynamically changes keys as it's being used, this ensures data integrity.

WPA also uses [[EAP|EAP]] (extensible authentication protocol) which verifies authorized network users.

### WPA2

This was developed to provide stronger security for wireless networks. Instead of [[TKIP|TKIP]] this uses [[CCMP|CCMP]] (Counter Cipher Mode w. Block Chaining Message Authentication Code Protocol) for encryption. This uses an "enchanced data crytographic encapsulation mechanism."

Since 2006, WPA2 is available on all certified Wi-Fi hardware.

## Wi-Fi Protected Setup (WPS)

![[Pasted image 20230421173109.png]]

>Above is an example of a WPS configuration page.

This protocol was designed for people that don't have a good nor any understanding of wireless networks so that they can easily join a protected network without having to worry about configuring anything important nor hard.

## MAC Filter

![[Pasted image 20230421173337.png]]

This is just a white/black list for MAC addresses which determines if a device with said MAC address is allowed to connect to the network or not. Really simple.

## Demilitarized Zone (DMZ)

![[Pasted image 20230421173704.png]]

This fully exposes a computer to the internet by forwarding all its ports. This is useful for when you're troubleshooting a [[Firewalls|firewall]] issue.

A computer in the DMZ **must** be assigned a static IP address and not one assigned dynamically via. a DHCP server.

## Port Forwarding

![[Pasted image 20230421174112.png]]

This is telling the router where to send requests to. If one computer outside the network wants to use RDP to view a computer on your network, you'll need to enable port forwarding on your router.
