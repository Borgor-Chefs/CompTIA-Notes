---
tags:
  - networking
  - protocol
---
# Network Address Translation (NAT)

This is a service typically used in [[Router|routers]] that maps one set of [[IP Address|IP addresses]] to another set of IP addresses:

- map [[IP Address#Private IP Address|private IPs]] addresses to public ones
- map [[IP Address#Public IPv4 Ranges|public IP]] addresses to private ones

![[Pasted image 20230331193312.png]]

## NAT Overload

>Also referred to as "Port Address Translation (PAT)".

![[Pasted image 20240320171708.png]]

NAT works just fine when there is one device on the network, it's a very simple process. But what happens then there's more than one computer/[[IP Address#Private IP Address|private IP]] on the same network?

Basically, the request from the [[IP Address#Private IP Address|private IP]] over a certain port number is saved in the [[Router]]'s NAT table. Once the response from the destination is received by the router, it will translate the [[IP Address#Public IP Address|public IP]] back to the private IP using this table.
