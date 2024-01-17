---
tags:
  - security
  - virtual
  - networking
---
# Access Control Lists (ACLs)

This is something software based that is used to allow or deny traffic, usually through a [[Networking Hardware#Routers|router]] or an [[Operating Systems Overview|operating system]].

## Routers

For routers, ACLs filter traffic on the following criteria (or more):

- source IP
- destination IP
- [[TCP]] port numbers
- [[UDP]] port numbers
- [[Networking Ports|protocols]] such as ICMP

The router, upon receiving a packet, will see if any of the packet's information matches an existing ACL and either allow or deny this traffic.

## Operating Systems

An ACL is useful when determining what users should have access to what parts of the filesystem. For instance, Joe from accounting should not be able to access the home folder of Bob from management or vice versa.
