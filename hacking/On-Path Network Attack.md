---
tags:
  - security
  - attack
  - networking
---
# On-Path Network Attack

>Formerly known as a "Man-in-the-middle" attack.

![[Pasted image 20240208125120.png]]

What the diagram shows here is an attacker taking advantage of a local subnet and the lack of security protocols with [[ARP]].

The attacker lies to the victim computer, telling it that it is the router (or some other host) and replies with it's own MAC address. The attacker will do the same for the router.

The result is that the attacker's computer will sit in the middle between all hosts and the router, this allows for packet sniffing, redirection, etc.

## Middle-Man On the Same Computer

This is where the attacker is using the same computer that you're using i.e., there's malware installed like a [[Trojan Horse]].

What could happen is the attacker monitors various applications on your computer (usually the browser) and will wait for anything interesting to happen. For example, the malware could lie dormant until you log into your banking website and then steal your credentials.
