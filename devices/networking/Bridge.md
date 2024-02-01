---
tags:
  - device
  - networking
---
# Bridges

![[Pasted image 20230322195501.png]]

>"Used to divide networks into separate collision domains."

Bridges are used to bridge networks together but they are ordinarily dumb and do not filter packets.

## Filtering Bridge

Filtering bridges do this exact thing, they filter off of MAC addresses and operate on level 2 of the [[OSI Model|OSI model]]. The filtering bridge can do this since they memorize the MAC addresses of all components connected to it. They are also mainly used to filter data within the same network.

This is also an inexpensive way of implementing a [[Router|router]] if one isn't available.
