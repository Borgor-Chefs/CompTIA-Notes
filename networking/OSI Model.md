# OSI (Open Systems Interconnection) Reference Model

>Reference video, [here](https://www.youtube.com/watch?v=owDh6FNJUog&list=PLG49S3nxzAnlCJiCrOYuRYb6cne864a7G&index=2).

This is a conceptual model that provides a common basis for the coordination of ISO standards development for the purpose of systems interconnection.

This is a guide and not the end all be all, it's a useful tool to describe how data is flowing over the network. Apparently, most of the protocols didn't catch on, somewhat proven by how we use [[TCP|TCP/IP]] for most of networking.

A good way to see the OSI model in action, is by using some packet sniffing software like WireShark.

![[Pasted image 20240311161543.png]]

>The above image shows WireShark.
>- frame 88 describes the [[#Physical Layer]]
>- ethernet II describes the [[#Data Link Layer]]
>- internet protocol describes the [[#Network Layer]]
>- transmission control protocol describes the [[#Transport Layer]]
>- secure socket layer describes the [[#Session Layer]], [[#Presentation Layer]] and the [[#Application Layer]] grouped into one

## Layers

Here are some things/services/protocols that run on each layer of the model and the purpose of each layer. There are seven layers to this model:

- 7. [[#Application Layer|application]] - what you see with your eyes
- 6. [[#Presentation Layer|presentation]] - application encryption (SSL, TLS)
- 5. [[#Session Layer|session]] - control protocols, tunneling protocols
- 4. [[#Transport Layer|transport]] - [[TCP]] segments, [[UDP]] datagrams
- 3. [[#network Layer|network]] - [[IP Address|IP addresses]], [[Router|routers]], packets
- 2. [[#Data Link Layer|data link]] - frames, [[MAC Addresses|MAC addresses]], extended unique identifiers, [[Switch|switches]]
- 1. [[#Physical Layer|physical]] - [[Cables|cables]], fiber, and the signal itself

>You can remember the OSI model by this mnemonic: "All People Seem To Need Data Processing".

Certain protocols do not explicitly nor cleanly map to a certain layer of the OSI model, [[USB]] for instance, does multiple things which do not cleanly map to a single layer.

>Read more about it from this response on [StackOverflow](https://stackoverflow.com/questions/61302045/classifying-usb-protocol-in-the-osi-model).

As an example to illustrate the connection to https://mail.google.com, here's what's happening at each layer:

- [[#Application Layer]]: the URL https://mail.google.com
- [[#Presentation Layer]]: the SSL encryption
- [[#Session Layer]]: links the presentation to the transport
- [[#Transport Layer]]: TCP encapsulation
- [[#Network Layer]]: IP encapsulation
- [[#Data Link Layer]]: ethernet
- [[#Physical Layer]]: electrical signals

### Application Layer

As humans, this is the layer that we can see.

Related protocols/technologies:

- [[DNS]]
- [[FTP]]
- [[HTTP]]
- [[LDAP]]
- [[SSH]]

### Presentation Layer

This layer deals with transforming the received data into something that humans can understand i.e., character encoding, application encryption/decryption, etc.

This layer is often combined with the [[#Application Layer]] because the functionality is so closely combined with our ability to use the applications.

Related protocols/technologies:

- MIME
- XDR
- PGP

### Session Layer

This layer deals with communication between devices i.e., start, stop and restart. Basically control and tunneling protocols. Once two devices have connected, they will start some form of session and then begin to transfer data.

Related protocols/technologies:

- [[NetBIOS]]
- SOCKS
- PPTP
- RTP

### Transport Layer

This is also known as the "post office" layer because of how it describes how data is being sent and where it is being sent to within a system/network. This layer primarily uses [[TCP]] and [[UDP]] for communication.

A good example to illustrate how this works is loading websites. Essentially, websites (usually) are too big to be sent over the network in a single frame and are therefore divided up and reassembled by the recipient computer.

Related protocols/technologies:

- [[TCP]]
- [[UDP]]
- SCTP
- DCCP
- SPX

### Network Layer

Also known as the "routing" layer, this layer deals with [[IP Address|IP addresses]] and communication between them. What will also happen is network frame fragmentation, this occurs to move data from an ethernet network, to a [[Network Types#Wireless LAN (WLAN)|WLAN network]] and to another ethernet network.

Related protocols/technologies:

- [[IP Address#Internet Protocol Address|IPv4/6]]
- ICMP
- IPX
- AppleTalk

### Data Link Layer

This is the "basic networking language" that all computers speak. All, if not then most protocols are built upon the ones found here. You might also hear these protocols referred to as the "data link control (DLC) protocols".

Finally, this layer is also referred to as the "switching" layer because [[Switch|switches]] make their decisions based upon the [[MAC Addresses|MAC address]] of the [[Network Interface Card|NIC]] of the computer.

Related protocols/technologies:

- ATM
- ARP
- [[MAC Addresses|MAC]]
- PPP
- HDLC

### Physical Layer

This is the physical layer of the network i.e., signalling, cabling, connectors and such. For example, if someone tells you "you have a physical layer problem", it could mean that you should:

- fix your cabling, punch-downs, etc.
- run loopback tests, test/replace cables, swap [[!Expansion Cards|adapter cards]], etc.
