---
tags:
  - interface
  - bus_slot
  - todo
---
# Peripheral Component Interconnect Express (PCIe)

>The main article about PCIe: [Wikipedia](https://en.wikipedia.org/wiki/PCI_Express).
>PCIe superseded PCI in 2004.

![[Pasted image 20231220152439.png]]

>From top to bottom:
>- PCIe x4
>- PCIe x16
>- PCIe x1
>- PCIe x16
>- PCI (32bit, 5V)

- supersedes
    - [[PCI]]
    - [[PCI#PCI Extended (PCI-X)|PCI-X]]
    - [[AGP]]

Developed in 2003 by [PCI-SIG](https://pcisig.com/), this was meant to replace PCI and AGP entirely and succeeded in doing so. This is now the standard bus slot you will find in modern computers (really any computer made after 2003).

>In modern computers, you will mainly deal with PCIe in [[The Motherboard|motherboards]] and miniPCIe in laptops.

There are varying sizes for PCIe slots and they are;

- PCIe x1, this has 1 lane for data
- PCIe x4, this has 4 lanes for data
- PCIe x8, this has 8 lanes for data
- PCIe x16, this has 16 lanes for data

>The PCIe x16 slot has succeeded the [[AGP|AGP]] slot for a [[Graphics Card|video card]], but you may still encounter AGP slots on older computers.

- older iterations - data transfers in parallel
    - [[PCI]] (was superseded by [[#PCI Express (PCIe)|PCIe]])
    - [[PCI#PCI Extended (PCI-X)|PCI-X]]
    - [[PCI#miniPCI|miniPCI]] (was superseded by [[#miniPCIe|miniPCIe]])

>PCIe is not backwards compatible with PCI slots since the two have very different architectures.

## Speeds

![[Pasted image 20231220153936.png]]

### miniPCIe

>From [Wikipedia](https://en.wikipedia.org/wiki/PCI_Express#MINI-CARD).

![[Pasted image 20231220154331.png]]

>Showcasing the size difference between [[PCI#miniPCI|miniPCI]] and miniPCIe.

Most laptops built after 2005 use PCIe for [[!Expansion Cards|expansion cards]] but many manufacturers are moving towards the new [[M2|M.2]] form factor.
