---
tags:
  - protocol
  - security
  - encryption
  - networking
---
# Wi-Fi Protected Access (WPA)

>See more [here](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access).

This is the security standard that is commonly used on all networking devices. The only standards that should be used are:

- [[#WPA2]]
- [[#WPA3]]

The rest are deemed insecure i.e., don't use [[#WPA]] nor [[WEP]].

## WPA

>Superseded by [[#WPA2]].

This is the precursor to [[#WPA2]] and should not be used as there is a similar flaw in WPA from [[WEP]] that renders this insecure.

WPA uses [[TKIP]] to check the integrity of packets (i.e. test if any of the data was altered), TKIP includes a [[MIC]] check. WPA replaced the use of [[CRC-32]] in favor of TKIP.

This protocol is insecure because the keystream can be retrieved from sending short packets to use for re-injection and spoofing.

## WPA2

>See more [here](https://en.wikipedia.org/wiki/IEEE_802.11i-2004).
>Superseded by [[#WPA3]] but still used.

Introduced in 2004, WPA2 requires the use of [[CCMP|CCMP block cipher mode]] and [[AES]] for encryption.

The packet is encrypted using AES and includes a [[MIC]] with [[CBC-MAC]] checksum for data integrity.

### The WPA2 PSK Problem

The PSK (pre-shared key) problem is quite severe nowadays because of the improvements to hash cracking and overall performance increases by technology. What can happen is a hacker can capture the hashed PSK from 4 way handshake between the client and the access point and brute force it to crack it.

This is the flow:

1. hacker sniffs packets from this network
2. hacker obtains the 4 way handshake packets that contain the hashed PSK
3. hacker brute-forces the hash to crack it
4. once cracked, the hacker returns to the site and can connect to the network

## WPA3

Introduced in 2018, WPA3 requires the use of [[GCMP]] and [[AES]] for encryption.

The packet is encrypted using AES and includes a [[MIC]] with [[GCMP#Galois Message Authentication Code (GMAC)|GMAC]] for data integrity.

### Simultaneous Authentication of Equals (SAE)

Because of the [[#The WPA2 PSK Problem]], WPA3 made security improvements. This improvement is called SAE (or sometimes called the dragonfly handshake) wherein both client and access point never share any key information over the network and both derive a session key to use.

This is a variation of the Diffie-Hellman key exchange. Because of this, there are no more four-way handshakes, no hashes nor brute force attacks that can be used to gain access to the network.

Every client uses a different session key but all use the same PSK. This is apart of the IEEE standard for WPA3.
