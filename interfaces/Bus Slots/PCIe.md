---
tags:
  - interface
  - bus_slot
  - todo
---
# Peripheral Component Interconnect Express (PCIe)

>The main article about PCIe: [Wikipedia](https://en.wikipedia.org/wiki/PCI_Express).
>Since PCI is no longer being used in production.

This is the modern bus type developed in 1993, supporting a 32-bit or 64-bit data path. PCI slots have a bandwidth between 133 MB/s and 533 MB/s. These are half the physical length of the older [[ISA|ISA]] slots.

- modern iteration - data transfers in serial
    - [[#PCI Express (PCIe)]]
    - [[#miniPCIe]]
- older iterations - data transfers in parallel
    - PCI (was superseded by [[#PCI Express (PCIe)|PCIe]])
    - [[#PCI Extended (PCI-X)]]
    - [[#miniPCI]] (was superseded by [[#miniPCIe|miniPCIe]])

>PCIe is one of the most common bus types you will see.
>In modern computers, you will mainly deal with PCIe in [[The Motherboard|motherboards]] and miniPCIe in laptops.

## PCI Express (PCIe)

>From [Wikipedia](https://en.wikipedia.org/wiki/PCI_Express).

The latest version of bus slots, meant to succeed all other bus (including the older version of PCI and [[!Bus Slots#Accelerated Graphics Port (AGP)|AGP]]) slots. A PCIe slot has a bandwidth of up to 4 GB/s and transfers data in serial in packets.

>PCIe is not backwards compatible with PCI slots since the two have very different architectures.

There are varying sizes for PCIe slots and they are;

- PCIe x1, this has 1 lane for data
- PCIe x4, this has 4 lanes for data
- PCIe x8, this has 8 lanes for data
- PCIe x16, this has 16 lanes for data

>The PCIe x16 slot has succeeded the [[AGP|AGP]] slot for a [[Graphics Card|video card]], but you may still encounter AGP slots on older computers.

### miniPCIe

>From [Wikipedia](https://en.wikipedia.org/wiki/PCI_Express#MINI-CARD).

## Older Iterations

These are the older iterations of the PCI slot which are outdated and no longer made in modern computer hardware.

### PCI Extended (PCI-X)

This is a physical extension of the old PCI slot and sports a 64-bit bus. This is backwards compatible with the PCI slot.

This was mainly designed for servers and high speed computers.

### miniPCI

This slot is used in laptops and is approximately 1/4 the size of a regular PCI slot. The miniPCI slot is a 32-bit, 33 MHz bus.

>It is possible to insert a miniPCI card into a PCI slot but, you'd have to use a miniPCI to PCI converter.

This was superseded by [[#miniPCIe]].
