---
tags:
  - motherboard
---
# The Motherboard

The main component of the computer where all of the components connect to. Such connectors include:

- the processor [[CPU Sockets|socket]] for the [[CPU]]
- memory slots for [[RAM Types]]
- [[!Bus Slots|bus slots]] for things such as a
	- [[Graphics Card]]
	- [[Network Interface Card]]
	- [[PCIe|PCIe]] devices
- [[Interfaces|I/O interfaces]] to connect external devices

Motherboards come in different sizes known as [[Motherboard Form Factors|form factors]]. The most common form factors are;

- [[Motherboard Form Factors#Advanced Technology eXtension (ATX)|ATX]]
- [[Motherboard Form Factors#Micro ATX|Micro ATX]]

>The ATX form factor is much more common.

## Front Panel Connector

This is the place where you plug in wires which connect that connect to the front bezel of the computer case. This grid is also color coded to aid in plugging in the wires. Some of these connectors include;

- power (green) & power LED (yellow)
- hard drive LED (red)
- reset (blue)
- speaker (orange)

## Chipsets

A chipset is a centralization for the numerous chips on a motherboard.

Older motherboards were littered with components (capacitors, resistors, etc.), but it's far simpler to centralize these components into a single chip known as a chipset.

Chipsets are divided into two components; the [[#North Bridge|north bridge]] and [[#South Bridge|south bridge]]. These are two independent chips with individual functions.

### North Bridge

The north bridge connects to the [[CPU|CPU]], [[PCIe|PCIe]]/[[AGP|AGP]] and memory slots via. connectors called [[Interfaces|buses]].

The north bridge operates at a higher speed than the south bridge and connects to more important components which need to operate at a higher speed.

### South Bridge

The south bridge connects to the [[PCIe|PCIe]], [[USB|USB]], [[eSATA Port|SATA]] and IDE slots via. buses. If the computer needs to access these things it will talk to the north bridge and then the south bridge.

The south bridge isn't as fast as the north since the connected components don't need to operate at as high a speed as [[RAM Types|RAM types]] or a [[PCIe|PCIe]] slot.
