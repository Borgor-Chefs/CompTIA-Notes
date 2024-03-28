---
tags:
  - networking
---
# Network Broadcasting Methods

These are ways in which a device communicates over the network to a number of devices.

## Unicast

![[Pasted image 20240327163957.png]]

>One to one.

Unicast is where one device is only communicating to one other device. This is good for file transfers or web surfing. This is a very common way to communicate and is used extensively with [[IP Address#IPv4|IPv4]] and [[IP Address#IPv6|IPv6]].

But, this is not optimal if a device needs to communicate to multiple devices simultaneously.

## Broadcast

![[Pasted image 20240327164146.png]]

>One to all.

This is a communication type where information i.e., packets are sent to everyone at once. However, there is a limited scope with this, called the "broadcast domain" which is usually just your subnet.

Broadcast is used in routing updates, [[ARP]] requests and only used with [[IP Address#IPv4|IPv4]] and not [[IP Address#IPv6|IPv6]] (IPv6 is for [[#Multicast]]).

Broadcast can actually cause performance issues on a [[Network Types#Local Area Network (LAN)|LAN]] due to the amount of information being broadcasted. IPv6 limits the scope of the transmitted information, thereby improving performance.

## Multicast

![[Pasted image 20240327164618.png]]

>One to many of many.

Unlike [[#Broadcast]], this type of communication is more efficient because only the interested parties will receive the information being broadcasted.

Multicast is used both in [[IP Address#IPv4|IPv4]] and [[IP Address#IPv6|IPv6]] but more extensively in IPv6.

This is a very specialized protocol and is difficult to scale across large networks.

## Anycast

![[Pasted image 20240327164849.png]]

>One to one of many. You can think of this as like; shortest path or fastest response.

This is where a single destination [[IP Address]] has multiple paths or two or more endpoints. This is used with [[IP Address#IPv4|IPv4]] and [[IP Address#IPv6|IPv6]].

The configuration for this type of broadcast looks like a [[#Unicast]] address. But it is in fact an anycast adress.

Packets sent to an anycast address are delivered to the closest interface.
