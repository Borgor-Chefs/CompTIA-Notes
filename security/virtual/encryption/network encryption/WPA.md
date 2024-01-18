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

The rest are deemed insecure.

## WPA

>Superseded by [[#WPA2]].

This is the precursor to [[#WPA2]] and should not be used as there is a similar flaw in WPA from [[WEP]] that renders this insecure.

WPA uses [[TKIP]] to check the integrity of packets (i.e. test if any of the data was altered), TKIP includes a [[MIC]] check. WPA replaced the use of [[CRC-32]] in favor of TKIP.

This protocol is insecure because the keystream can be retrieved from sending short packets to use for re-injection and spoofing.

## WPA2

>See more [here](https://en.wikipedia.org/wiki/IEEE_802.11i-2004).

Introduced in 2004, WPA2 requires the use of [[CCMP]] and [[AES]] for encryption.

The packet is encrypted using AES and includes a [[MIC]] with [[CBC-MAC]] for data integrity.

## WPA3

Introduced in 2018, WPA3 requires the use of [[GCMP]] and [[AES]] for encryption.

The packet is encrypted using AES and includes a [[MIC]] with [[GCMP#Galois Message Authentication Code (GMAC)|GMAC]] for data integrity.
