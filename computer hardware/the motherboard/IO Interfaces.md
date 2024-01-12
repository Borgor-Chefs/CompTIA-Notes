Tags: [#motherboard]

# Input/Ouput Interfaces

![[Pasted image 20220814171316.png]]

On a motherboard there is a grouping of ports (interfaces) on one side of the motherboard to be exposed through the PC case.

These interfaces (also called ports) include the;

- [[#^ccf692|PS/2 Port]]
- [[#^1d9a68|USB Port]]
- [[#^b1183e|Serial Port]]
- [[#^a3d109|Parallel Port]]
- [[#^ce8d37|Video Adaptor]]
	- [[#^9415c9|VGA Port]]
	- [[#^6370bf|DVI Port]]
	- [[#^fd6bbc|HDMI Port]]
	- [[#^95fc90|DisplayPort]]
- [[#^cd3743|Firewire Port]] (IEEE Port)
- [[#^519428|Network Port]]
- [[#^af1c39|Sound Ports]]
- [[#^3b0554|eSATA Port]]

## PS/2 Port

^ccf692

The PS/2 port is a 6 pin - multi-din connector. An older technology which is being phased out for USB technology.

These ports have coloring where;

- Green is for a mouse
- Purple is for a keyboard

There are variations of this port where the individual keyboard and mouse ports are merged into one. One half being green and the other being purple.

## Universal Serial Bus (USB) Port

^1d9a68

This is the most common type of connector external devices will use to connect to your computer. [[The Motherboard|Motherboards]] will have a lot of these. The USB port also provides power to the input device.

- USB 1.0 has a transfer speed of 1.5 Mb/s (megabits) (1996)
- USB 1.1 has a transfer speed of 12 Mb/s (1998)
- USB 2.0 has a transfer speed of 480 Mb/s (2000)
- USB 3.0 has a transfer speed of 5 Gb/s (gigabits), the port is usually blue (2008)
	- USB 3.1 has a transfer speed of 5 Gb/s
	- USB 3.2 Gen 1 has a transfer speed of 5 Gb/s
	- this is the last version to support the Type A connector
- USB 3.2 has a transfer speed of 20 Gb/s (2017) which comprises
	- USB 3.2 Gen 1x2
	- USB 3.2 Gen 2x2
	- requires the Type C connector
- USB 4.0 announced in 2019 is based on the Thunderbolt 3 protocol
	- it supports up to 40 Gb/s and is compatible with USB 3.2 and USB 2.0

## Serial Port

^b1183e

The serial port is an older technology which was mainly used for terminals and modems. This port is being phased out for the faster [[#^1d9a68|USB]] port

This port sends data one by one. The most common interface of a serial port is the RS-232 port with the Type D connector

## Parallel Port

^a3d109

The parallel port is mainly used for connecting printers. This sends multiple streams of data over different connectors simultaneously. This is being phased out for the faster [[#^1d9a68|USB]] port.

This uses a D-sub connector known as the DB-25 connector

## Video Adaptor

^ce8d37

If a video adaptor is present, the motherboard has integrated video. Where the interface and the motherboard are one.

Integrated video usually isn't very high performance, because of this people will usually buy a [[Video Card|graphics card]] to support their needs (which is usually gaming or rendering).

The most common video adaptors are:

- [[#^9415c9|VGA]]
- [[#^6370bf|DVI]]
- [[#^fd6bbc|HDMI]]
- [[#^95fc90|DisplayPort]]

### Video Graphics Array (VGA)

^9415c9

![[Pasted image 20220827163552.png]]

Designed in 1987, this port carries analog data and is usually colored blue and has 15 pins divided into 3 rows. This indicates a low performance video card. This port was superceded by the faster [[#^6370bf|DVI]] port.

### DVI

^6370bf

![[Pasted image 20220827163603.png]]

Developed in 1999, this type of port was designed by the Digital Display Working Group (DDWG) and is used to connect a video output device such as a video display controller or to a display device such as a computer monitor.

This interface was designed to transmit uncompressed digital video and comes in difference variations;

- DVI-A for analog data only
- DIV-D for digital data only
- DVI-I for digital and analog data

This port was superceded by the [[#^fd6bbc|HDMI]] and [[#^95fc90|DisplayPort]] ports.

### HDMI

^fd6bbc

![[Pasted image 20220827163609.png]]

Designed in 2002, this port superceded the [[#^6370bf|DVI]] and [[#^9415c9|VGA]] ports. HDMI is a proprietary audio/video interface that transmits uncompressed video and either compressed or uncompressed audio data from an HDMI compliant source to an HDMI compliant output such as a display controller or to a compatible monitor, video projector, TV or digital audio device.

HDMI is the digital replacement for analog video standards. HDMI has 19 pins and a bitrate of 48 Gbit/s (as of HDMI 2.1a).

HDMI became the de facto standard for HDTVs and is one of the most common ports you will encounter.

### DisplayPort

^95fc90

![[Pasted image 20220827173155.png]]

Designed in 2006, this port also superceded the [[#^6370bf|DVI]] and [[#^9415c9|VGA]] ports. This technology relies on packetized data transmission like ethernet, [[#^1d9a68|USB]] and [[Bus Slots#^93c132|PCIe]]. DisplayPort can carry video, audio, USB and other forms of data.

DisplayPort can be used to transmit audio and video simultaneously although both can be transmitted without the other.

This port is also backwards compatible with interfaces such as [[#^6370bf|DVI]] or [[#^fd6bbc|HDMI]] via. either active or passive adapters.

## Firewire (IEEE) Port

^cd3743

The firewire port (or the IEEE port) is commonly used to attach cameras or printers. This type of port isn't nearly as common as the [[#^1d9a68|USB]] port and a lot of [[The Motherboard|motherboards]] will not have this type of port.

You can recognize this port by its D shape. Fireware has transfer speeds up to 400 Mb/s (less than USB 2.0).

## Network Port

^519428

The [[Network Interface Card|Network Interface Card]] (NIC) is used for networking purposes, this has a port which fits a [[Cables and Connectors#^459cd4|RJ-45]] connector (ethernet cable). The purpose of this port is to provide a constant connection to a network.

The bandwidth ranges from 10 to 1000 Mb/s. Each NIC has a unique identifier known as a MAC address.

## Sound Ports

^af1c39

Sound ports are for audio devices such as headphones, microphones or a speaker. The [[Sound Card|sound card]] processes audio and transmits it through a computer's speakers.

If a [[The Motherboard|motherboard]] has these ports present, it means that it has a sound card built in. This is known as integrated sound.

A basic [[Sound Card|sound card]] will have a green port for speakers and a pink one for a microphone, however more sophisticated sound cards will have more ports for subwoofers, etc.

## eSATA Port

^3b0554

The external [[HDD#^20a48d|SATA]] port (eSATA) which is used for attaching external SATA drives. This also functions similarly to [[#^1d9a68|USB]] and [[#^cd3743|Firewire]] ports. Transfer speeds are faster but it requires its own power plug.

Another port called the eSATAp port combines data transfer and power in, all in one port.
