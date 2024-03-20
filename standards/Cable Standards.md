---
tags:
  - networking
  - standard
  - cable
---
# Cable Standards

>See more about TIA [here](http://tiaonline.org)

These are the wiring standards created by the Telecommunications Industry Association (TIA), namely:

- [[#T568a|ANSI/TIA-568a]]
- [[#T568b|ANSI/TIA-568b]]

>The international ISO/IEC 11801 cabling standards define classes of networking standards, not cabling standards which are discussed in this note.

These standards define how the "[[Digital Cables#Twisted Pair Cables|twisted pair cables]]" (colored wires) should be connected to an [[Digital Cables#Register Jack 45 (RJ-45) (Ethernet Cable)|RJ-45]] connector. There is no difference in functionality between both standards.

There are also types of cables which refer to what standard both ends of the wire follow:

- the most wiring standard is a [[#Straight Cable|straight cable]]
- the [[#Cross-over Cable|cross-over cable]]
- the [[#Rollover Cable|rollover cable]]
- the [[#Loopback Cable|loopback cable]]

## Standards

It's important to note that you should never mix both of these standards in one cable, this will lead to much confusion and technical problems.

### T568a

See below how the wiring should look like for the T568a standard:

![[Pasted image 20240317165711.png]]

### T568b

See below how the wiring should look like for the T568b standard:

![[Pasted image 20240317165720.png]]

Many organizations traditionally use this standard for their cabling.

## Cable Types

### Straight Cable

This means that both ends of the cable follow the same standard, this is the most common type of cable and it is used to connect computers to hubs, switches or modems.

![[Pasted image 20230322184717.png]]

### Cross-over Cable

This is where each end is wired differently and are used to connect two similar devices together such as two computers together without using a hub or a switch. They are also used to connect hubs and switches together.

![[Pasted image 20230322184943.png]]

>Cross-over cables are defined in the IEEE 11803 standard and not the 11801 standard.

### Rollover Cable

This is created when both ends are wired completely opposite of each other. This is used to connect a compueter or a terminal to a router's console port.

![[Pasted image 20230322185032.png]]

### Loopback Cable

This is used to testing purposes, namely to trick the computer into thinking that it's connected to a network. To create a loopback cable, connect pin 1 to pin 3 and pin 2 to pin 6.

![[Pasted image 20230322185206.png]]
