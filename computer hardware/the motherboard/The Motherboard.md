Tags: [#motherboard]

# The Motherboard

The main component of the computer where all of the components connect to. Such connectors include:

- the processor [[CPU Sockets|socket]] for the [[CPU]]
- memory slots for [[RAM]]
- [[Bus Slots|bus slots]] for things such as a
	- [[Video Card]]
	- [[Network Interface Card]]
	- [[Bus Slots#^93c132|PCIe]] devices
- [[IO Interfaces|I/O interfaces]] to connect external devices

Motherboards come in different sizes known as [[Motherboard Form Factors|form factors]]. The most common form factors are;

- ATX
- Micro ATX 

The ATX form factor is much more common.

## Front Panel Connector

This is the place where you plug in wires which connect that connect to the front bezel of the computer case. This grid is also color coded to aid in plugging in the wires. Some of these connectors include;

- power (green) & power LED (yellow)
- hard drive LED (red)
- reset (blue)
- speaker (orange)

## Chipsets

A chipset is a centralization for the numerous chips on a motherboard.

Older motherboards were littered with components (capacitors, resistors, etc.), but it's far simpler to centralize these components into a single chip known as a chipset.

Chipsets are divided into two components; the [[#^2ac5f3|north]] bridge and [[#^472225|south bridge]]. These are two indepent chips with individual functions.

### North Bridge

^2ac5f3

The north bridge connects to the [[CPU|CPU]], [[Bus Slots#^93c132|PCIe]]/[[Bus Slots#^71e47d|AGP]] and memory slots via. connectors called [[Bus Slots|buses]].

The north bridge operates at a higher speed than the south bridge and connects to more important components which need to operate at a higher speed.

### South Bridge

^472225

The south bridge connects to the [[Bus Slots#^da289e|PCI]], USB, SATA and IDE slots via. buses. If the computer needs to access these things it will talk to the north bridge and then the south bridge.

The south bridge isn't as fast as the north since the connected components don't need to operate at as high a speed as [[RAM|RAM]] or a [[Bus Slots#^93c132|PCIe]] slot.
