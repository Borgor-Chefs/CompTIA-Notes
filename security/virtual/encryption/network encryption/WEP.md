---
tags:
  - protocol
  - networking
  - security
  - encryption
---
# Wired Equivalent Privacy (WEP)

>See more [here](https://en.wikipedia.org/wiki/Wired_Equivalent_Privacy).
>This is unsecure and has been replaced with [[WPA#WPA|WPA]].

This is know known as a "severely flawed" security algorithm for [[802.11]] wireless networks and was ratified in 1997.

Standard 64-bit WEP uses a 40-bit key which is concatenated with an 24-bit initialization vector (IV) to form its RC4 key. This key would then be XOR'd with the plaintext to produce the ciphertext which is then broadcasted over the network.

It also uses a [[CRC-32|CRC-32 checksum]] for integrity.

## Security Flaws

Why is this a bad protocol? Ultimately, there is a 50% chance that the same IV will repeat after 5,000 packets. The strategy is that an attacker would send a flood of encrypted ARP requests and try to obtain the shared authentication key being used, allowing them to obtain the key in less than 6 minutes.
