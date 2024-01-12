---
tags:
  - networking
---
# Network Components

These are typical hardware components you'll see in the field.

- [[#Firewalls|firewall]]
	- [[#Host Based|host based]]
- [[#Modems|modem]]
- [[#Hubs|hub]]
- [[#Switches|switch]]
- [[#Bridges|bridge]]
	- [[#Filtering Bridge|a filtering bridge]]
- [[#Routers|router]]
- [[Network Interface Card|network interface card]]
- [[#Wireless Access Point (WAP)|wireless access point]]
- [[#Patch Panels|patch panel]]

Some types of network components use Power over Ethernet (PoE) to supply power to the device. Some devices do not have this feature and they will instead have an interface to receive power.

## Components

### Firewalls

A firewall is a piece of software or hardware which filters incoming traffic into a private network. This blocks unwanted traffic and permits wanted traffic based on its access roles.

This is an essential piece of tech which almost all businesses use to keep their network safe.

There are different types of firewalls:

- [[#Host Based|host based]]

#### Host Based

This is a software firewall, installed on computer that only protects the computer. This will determine whether or not local traffic from the computer is allowed to leave the computer and communicate with the outside world. The "host based" name comes from the "host" being an application or program.

### Modems

![[Pasted image 20230322194846.png]]

This is a typical broadband cable modem, usually called DOCSIS (Data Over Cable Service Interfacer Specifications). This supports speeds of 10 Gigabit downstream and 1 Gigabit upstream. This handles both incoming and outgoing data signals.

![[Pasted image 20230322200842.png]]

There are also expansion modem cards which are used to transmit and receive analog data which comes from telephone lines. The job of this card is to convert analog data to digital data. The maximum speed of most modems today is 56 Kbps.

### Hubs

![[Pasted image 20230322194855.png]]

These are "dumb" devices in the sense that it does not care where data is sent nor does it filter any data like a firewall, the purpose of the hub is to copy all data from one [[Digital Cables#Register Jack 45 (RJ-45) (Ethernet Cable)|ethernet]] connection over to all other active ethernet connections.

There are two types:

- passive - doens't require a power source
- active - does require a power source

### Switches

![[Pasted image 20230322195223.png]]

Unlike [[#Hub|hubs]], switches are intelligent, they memorize the addresses of connected devices and only send data to and from different addresses based on their configuration. The goal of a switch is to reduce the amount of traffic on a network.

Switches operate on level 2 of the OSI model and they filter ethernet packets based on the MAC addresses contained within the packet.

### Bridges

![[Pasted image 20230322195501.png]]

"Used to divide networks into separate collision domains."

Bridges are used to bridge networks together but they are ordinarily dumb and do not filter packets.

#### Filtering Bridge

Filtering bridges do this exact thing, they filter off of MAC addresses and operate on level 2 of the OSI model. The filtering bridge can do this since they memorize the MAC addresses of all components connected to it. They are also mainly used to filter data within the same network.

This is also an inexpensive way of implementing a router if one isn't available.

### Routers

![[Pasted image 20230322195731.png]]

This piece of hardware routes packets from one network to another based on the source and destination IP address. When a data packet is received, the router will inspect the packet and determine if the packet was meant for its network or another network.

![[Pasted image 20230322200039.png]]

If the router determines that the data packet is meant for its network then it will receive it and pass it along to the proper device, if not it will send the packet off to another network. This is essentially the gateway for the network.

In the above example, the router will only accept data packets colored red since this is traffic meant for this network. If not, the router will pass the data along to other networks. Keep in mind, this is a very simplified example.

### Wireless Access Point (WAP)

![[Pasted image 20230322200718.png]]

This provides network connectivity from a wireless device to a network. You'd connect a WAP to a switch or router in order to provide wireless devices so that wireless devices can connect to a network.

### Patch Panels

![[Pasted image 20230322201008.png]]

This is a panel that has multiple cable connectiosn and connects incoming and outgoing patch cables in LAN.

This is very handy for network administrators to rearrange connections at ease.
