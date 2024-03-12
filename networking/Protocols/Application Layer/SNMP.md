---
tags:
  - networking
  - application_layer
  - osi
---
# Simple Network Management Protocol (SNMP)

>[[Networking Ports|Standard port]]: 161/162 (trap)
>[Link](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol).


This is used for network management and is primarily used to collect dat from various network devices such as: routers, printers and servers.

Apparently, this is a poorly secured protocol and there have been a number of CVEs associated with this protocol.

## Secure SNMP

>[[Networking Ports|Standard port]]: 10161/10162 (trap)

According to [this](http://www.net-snmp.org/wiki/index.php/Strong_Authentication_or_Encryption), SNMPv3 uses AES192 and AES256 for encryption over TLS.
