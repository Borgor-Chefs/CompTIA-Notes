---
tags:
  - networking
---
# Network Types

These are the types of networks that are largely classified by their size and geographical distribution.

>See more from Wikipedia [here](https://en.wikipedia.org/wiki/Wireless_LAN).

Here are the most common types (in terms of geographical size):

- [[#Peer-to-Peer Network (PTP)]]
- [[#Client-Server]]
- [[#Virtual Private Network (VPN)]]
    - [[#Dynamic Multipoint VPN (DMVPN)]]
- [[#Personal Area Network (PAN)]]
- [[#Local Area Network (LAN)]]
	- [[#Storage Area Network (SAN)]]
	- [[#Wireless LAN (WLAN)]]
	- [[#Virtual LAN (VLAN)]]
- [[#Campus/Corporate Area Network (CAN)]]
- [[#Metropolitan Area Network (MAN)]]
- [[#Wide Area Network (WAN)]]
    - [[#Software-Defined WAN (SD-WAN)]]

## Peer-to-Peer Network (PTP)

![[Pasted image 20240312185207.png]]

In such a network, there is no central server nor client. Every device in this network is both a client and a server.

The advantages are:

- easy to deploy: all that's required is some application with such functionality
- low cost: you don't need a central server

The disadvantages are:

- difficult to administer: no single computer governs the application
- difficult to secure: no single computer authenticates the connections/users

## Client-Server

![[Pasted image 20240312185338.png]]

In this type of network, all clients communicate with the server, no client directly communicates to another client.

The advantages are:

- performance: of the direct connection
- administration: you have a single object that requires administration instead of, for example, 20

The disadvantages are:

- cost: you need a server, a place for the server, a reliable internet connection, etc.
- complexity: you actually need to monitor and manage the server, unlike a [[#Peer-to-Peer Network (PTP)|PTP]] network

## Virtual Private Network (VPN)

This is essentially an encrypted tunnel which sends and receives traffic to and from a server located (usually) in another country which then gets routed to the actual destination.

The goal of a VPN is to have this server (which functions as a relay) to make the connection to the website, resource, etc. for you. This is a method of obscuring your real IP address.

### Dynamic Multipoint VPN (DMVPN)

![[Pasted image 20240312193349.png]]

This is often useful for communicating between sites, essentially, a VPN is created to tunnel traffic between sites and are built dynamically and on-demand. The VPN can also build and rebuild itself if there are any breaks in the connection.

The technique that this type of connection is built-upon is [[Multipoint Generic Router Encapsulation]].

The reason why this is useful is because you are not sending data nor maintaining the connection when you don't need to. You are also sending data directly, not going through a main access point/main office.

## Personal Area Network (PAN)

![[Pasted image 20230421163550.png]]

This is a very small network that are used to connect laptops, phones, printers, etc. together.
Generally used to transfer small files such as images, videos, audio, etc.

These networks operate using one of the following wireless transfer methods:

- [[Bluetooth]]
- [[Infrared]]
- [[NFC]]

Some examples of a PAN are:

- connecting your [[Bluetooth]] headset to your computer
- connecting your phone to your car
- connecting a FitBit to your phone

## Local Area Network (LAN)

![[Pasted image 20230421163602.png]]

A small network that consists of computers, printers, servers, etc. all physically located within the same building.

The most common type of LAN is an ethernet LAN where all devices are connected via. [[Ethernet Standard#Cable Categories|CAT 5 ethernet cable]] to a [[Switch|switch]].

### Storage Area Network (SAN)

>They are primarily used to access data storage devices, such as disk arrays and tape libraries from servers so that the devices appear to the operating system as direct-attached storage.
>[Wikipedia](https://en.wikipedia.org/wiki/Storage_area_network)

This is a dedicated network comprised of only [[!Storage Devices|storage devices]]. 

There is a difference between a network attached storage device (NAS) and a SAN. A NAS provides file-level access, meaning that any change to a file has to rewrite the whole file on the NAS. A SAN provides block-level access, meaning that if a single byte in a file changes, the whole file would not be changed, just that one byte.

These networks require a lot of bandwidth and may use an isolated network and high-speed networking technologies.

### Wireless LAN (WLAN)

>[Wikipedia](https://en.wikipedia.org/wiki/Wireless_LAN)

This is a regular [[#Local Area Network (LAN)|LAN]] but it is wireless, using Wi-Fi to connect devices together. These are generally [[802.11]] networks.

You can expand the coverage of this network with additional [[Wireless Access Point|access points]], such as multiple buildings or a university campus.

### Virtual LAN (VLAN)

>See more about [[Virtual Networks]].

This is essentially a partitioned network within a [[#Local Area Network (LAN)|LAN]] to separate traffic at the data link layer of the [[OSI Model#Data Link|OSI model]].

## Campus/Corporate Area Network (CAN)

This type of network is located within a limited geographical area that isn't as big as a [[#Metropolitan Area Network (MAN)|MAN]], primarily found in large corporations or universities or schools.

They communicate using LAN technologies such as fiber connected, high-speed ethernet. This is done over *private* land and by the company/university themselves, without a 3rd-party.

There would still be a monthly payment to an [[Internet Access Technologies|ISP]].

## Metropolitan Area Network (MAN)

![[Pasted image 20230421163618.png]]

>This type of network is larger than a [[#Local Area Network (LAN)|LAN]] but smaller than a [[#Wide Area Network (WAN)|WAN]].

This larger than a [[#Local Area Network (LAN)|LAN]] network because this spans multiple buildings within the same city or town. MANs are typically connected via. fiber optic cable or another highspeed medium.

Usually you're working with a 3rd-party provider for this connectivity such as a company like Bell or Telus.

Governments typically use these networks because their offices and buildings span large geographical areas. They also have the power to put [[Fiber Optic Cables|fiber optic cables]] really anywhere they want to give them the connectivity that they need.

## Wide Area Network (WAN)

![[Pasted image 20230421163518.png]]

This is a large area network which spans a large geographical area such as cities, nationwide, continent wide or globally. A great example of this is the internet.

These are generally slower than [[#Local Area Network (LAN)|LANs]] because of the physical distance and number of hops traffic must go through in order to reach its destination.

There are many different WAN technologies such as:

- point-to-point serial
- [[Multiprotocol Label Switching|MPLS]]
- terrestrial and non-terrestrial i.e., [[Internet Access Technologies#Satellite|satellite communication]]

### Software-Defined WAN (SD-WAN)

![[Pasted image 20240312194008.png]]

Basically, with newer [[!Cloud|cloud]] based technologies and many companies using them. It can be more efficient to communicate directly with the cloud and not going through a hop at, say, a data center.

The determination of how the data is routed is done by the WAN.

>How exactly? Honestly no idea, probably by [[DNS]] in conjunction with [[Networking Ports|poter numbers]].
