# Peripheral Component Interconnect (PCI)

>From [Wikipedia](https://en.wikipedia.org/wiki/Peripheral_Component_Interconnect).

![[Pasted image 20231220153343.png]]

>Shows three 5V 32-bit PCI slots.

- supersedes
    - [[ISA]] bus slots
- superseded by
    - [[AGP]] for graphics in 1997
    - [[PCIe]] in 2004

This is the older iteration of the modern bus type developed in 1992, supporting a 32-bit or 64-bit data path. PCI slots have a bandwidth between 133 MB/s and 533 MB/s. These are half the physical length of the older [[ISA|ISA]] slots.

This bus slot transfers data in parallel, whilst the newer [[PCIe]] slot transfers data in serial.

### PCI Extended (PCI-X)

This is a physical extension of PCI and sports a 64-bit bus. This is backwards compatible with the PCI slot.

This was mainly designed for servers and high speed computers.

### miniPCI

This slot is used in laptops and is approximately 1/4 the size of a regular PCI slot. The miniPCI slot is a 32-bit, 33 MHz bus.

>It is possible to insert a miniPCI card into a PCI slot but, you'd have to use a miniPCI to PCI converter.

This was superseded by [[PCIe#miniPCIe|miniPCIe]].
