---
tags:
  - storage
  - flash
---
# Flash Memory

>From [Wikipedia](https://en.wikipedia.org/wiki/Flash_memory).

Flash memory is an "electronic non-volatile computer memory storage medium" that can be wiped and reprogrammed. Flash memory can be used for both volatile and non-volatile purposes, along with being a pure storage device (like an [[SSD]]) or something that just holds a program.

There are two types of flash storage, NOR and NAND flash which reflect their internal logical NOR and NAND gates.

Flash memory also requires a controller, whether it is apart of the flash storage itself or a software driver that does the reading and writing from the drive itself. Things like [[SSD]], [[USB Stick|USB sticks]] and [[SD Card|SD cards]] are examples of flash memory and they have their own controller that performs "wear leveling" and error correction.

If your flash memory device has a controller, there's really no benefit to add a software specific flash memory [[File Systems|file system]] as the controller performs this task already.

>I know for a fact that I can put a non-flash memory file system onto a USB stick and SSD.

## Types of Storage

>See more [here](https://en.wikipedia.org/wiki/Multi-level_cell).

Flash memory operates using cells, these are just places that store 1s or 0s. But there are different types of cells, whose main difference is the amount of bits they can store per one cell.

- Single-level Cell (SLC) stores 1 bit per cell
- Multi-level Cell (MLC) stores 2 bits per cell
    - there is also the Double-level Cell which does the same thing as MLC
- Triple-level Cell (TLC) stores 3 bits per cell
- Quad-level Cell (QLC) stores 4 bits per cell
- Penta-level Cell (PLC) stores 5 bits per cell

>From what I can tell, this technology aims to make the flash memory device about the same physical size whilst optimizing the underlying components to increase the amount of digital storage.
