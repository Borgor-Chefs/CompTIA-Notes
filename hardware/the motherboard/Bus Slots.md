Tags: [#motherboard #expansion_card]

# Bus Slots / Expansion Slots

All [[The Motherboard|motherboards]] are equipped with input/output bus slots that are typically located at the bottom rear of the board connected to the [[The Motherboard#^472225|south bridge]].

They are also called expansion slots since you can add a expansion card to extend the functionality of your computer. For example you could add...

- a [[Sound Card|sound card]]
- a [[Network Interface Card|network card]]

## Types of Bus Slots

There are several types of bus slots such as:

- ISA
- [[#^da289e|PCI]]
	- [[#^013edd|PCI-X]]
	- [[#^f641a1|miniPCI]]
- [[#^71e47d|AGP]]
- [[#^93c132|PCIe]]

The modern bus type being [[#^93c132|PCIe]].

### Peripheral Component Interconnect (PCI)

^da289e

This is the modern bus type developed in 1993, supporting a 32-bit or 64-bit data path. PCI slots have a bandwidth between 133 MB/s and 533 MB/s. These are half the physical length of ISA slots.

This slot transfers data in parallel.

#### PCI Extended (PCI-X)

^013edd

This is a physical extension of the old [[#^da289e|PCI]] slot and sports a 64-bit bus. This is backwards compatible with the PCI slot.

This was mainly designed for servers and high speed computers.

#### miniPCI

^f641a1

This slot is used in laptops and is approximately 1/4 the size of a regular [[#^da289e|PCI]] slot. The miniPCI slot is a 32-bit, 33 MHz bus.

You can insert a [[#^da289e|PCI]] card into a miniPCI slot but you have to use a miniPCI to PCI converter.

### PCI Express (PCIe)

^93c132

The latest version of bus slots, meant to succeed all other bus slots. A PCIe slot has a bandwidth of up to 4 GB/s and transfers data in serial in packets.

PCIe is not backwards compatible with [[#^da289e|PCI]] slots since the two have very different architectures.

#### PCIe Sizes

There are varying sizes for PCIe slots and they are;

- PCIe x1, this has 1 lane for data
- PCIe x4, this has 4 lanes for data
- PCIe x8, this has 8 lanes for data
- PCIe x16, this has 16 lanes for data
	- This slot has succeeded the [[#^71e47d|AGP]] slot for a [[Video Card|video card]].

### Accelerated Graphics Port (AGP)

^71e47d

Created to assist in accelerating 3D graphics and is faster than the [[#^da289e|PCI]] slot because it has its own dedicated pathway to the processor (via. the [[The Motherboard#^2ac5f3|north bridge]]). This slot is only used for a [[Video Card|video card]].

This slot is usually colored brown.