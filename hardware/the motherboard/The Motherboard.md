# The Motherboard

The main component of the computer where all of the components connect to. Such connectors include:

- the processor socket for the [[CPU]]
- memory slots for [[RAM]]
- bus slots for things such as a
	- [[Video Card]]
	- [[Network Interface Card]]
	- PCI-E devices

The most common form factors for motherboards are the ATX and Micro ATX form factor. Although ATX is much more common.

## Form Factor

^aefe3b

This is a list of dimensions and designs of motherboards

- AT which stands for Advanced Technology
	- created in 1980s by IBM
	- superceded by the ATX form factor
	- 12 inches by 13.8 inches
- ATX which stands for Advanced Technology eXtension
	- created in 1995 by Intel
	- the standard form factor for PCs today
	- 12 inches by 9.6 inches
- Micro ATX is designed for smaller computer cases
	- they also have fewer features and consume less power than an ATX motherboard
	- 9.6 inches by 9.6 inches
- BTX is meant to be the successor to the ATX motherboard
	- designed by Intel
	- improved air flow design
	- flexible design which works in large and smaller cases
	- this motherboard takes advantage of newer technologies such as
		- USB 2.0
		- PCI-E
		- SATA
- ITX which is designed for smaller, space saving computers
	- designed by VIA Technologies
	- they consume less power and are often only cooled by heat sinks (no fans)
	- there are four models of ITX
		- Mini ITX
			- created in 2001
			- used for space saving computers
		- Nano ITX
			- created in 2005
			- designed to be used in digital recorders, media centers and cars
		- Pico ITX
			- created in 2007
		- Mobile ITX
			- created in 2009
			- 6cm by 6cm
- NLX created Intel, designed for low-end / low profile computers
	- utilizes a riser card which has slots to plug in extra components in parallel
	- typically found in slim line computer cases

## I/O Interfaces

![[Pasted image 20220814171316.png]]

On a motherboard there is a grouping of ports (interfaces) on one side of the motherboard to be exposed through the PC case.

- PS/2, 6 pin - multi-din connector
	- An older technology which is being phased out for USB technology
	- Green is for a mouse
	- Purple is for a keyboard
- USB connector
	- USB stands for Universal Serial Bus
	- Motherboards will have a lot of these
	- The USB port also provides power to the input device
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
- Serial Port is an older technology which is mainly used for terminals and modems
	- this sends data one by one
	- this is being phased out for the faster USB port
	- the most common interface of a serial port is the RS-232 port with the Type D connector
- Parallel Port is mainly used for connecting printers
	- this sends multiple streams of data over different connectors simultaneously
	- this is being phased out for the faster USB port
	- this uses a D-sub connector known as the DB-25 connector
- Video Adaptor 
	- if this is present, the motherboard has integrated video. Where the interface and the motherboard are one. Here are some common integrated video adapters
	- Integrated Video Adapters
		- integrated video usually isn't very high performance, because of this people will usually buy a [[Video Card]] to support their needs (which is usually gaming or rendering)
		- the VGA port 
			- carries analog data
			- usually colored blue and has 15 pins divided into 3 rows
			- this is a lower performance video card
- IEEE Connector or Firewire
	- recognized by its D shape
	- commonly used to attach cameras or printers
	- this is not nearly as common as USB and a lot of motherboards don't have this
	- Fireware has transfer speeds up to 400 Mb/s (less than USB 2.0)
- the [[Network Interface Card|Network Interface Card]] (NIC) is used for networking purposes
	- this has a port which fits a RJ-45 or ethernet cable
	- this provides a constant connection to a network
	- each NIC has a unique identifier known as a MAC address
	- transfer speeds range from 10 to 1000 Mb/s
- Sound card which processes audio through a computer's speakers
	- a basic sound card will have a green port for speakers and a pink one for a microphone
	- more sophisticated sound cards will have more ports for subwoofers, etc.
	- if the motherboard has a sound card built in this is known as integrated sound
- external SATA port (eSATA) which is used for attaching external SATA drives
	- functions similar to USB and Firewire ports
	- transfer speeds are faster but it requires its own power plug
	- another port called the eSATAp port combines data transfer and power in, all in one port

## Adapter / Expansion Card

^b294eb

![[Pasted image 20220814171258.png]]

The motherboard has multiple expansion slots that circuit boards can be installed within. These circuit boards, also known as adapter/expansion cards are meant to increase the functionality of the computer.

Some examples of these cards include:

- [[Video Card|video cards]]
- [[Sound Card|audio cards]]
- storage cards
- [[Network Interface Card|networking cards]]

See the `expansion cards` directory for more