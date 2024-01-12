---
tags:
  - storage
  - os
---
# Device Partitioning

This is a way to partition the total storage space of a device into smaller/larger blocks. This is useful for when you want different things such as:

- operating systems
- file systems
- encrypted file systems

All in their own space on your disk. A common term for these partitions are "volumes" (coming from Microsoft).

## Partition Styles

As of 2023, there are only two disk partition formats, they are:

- [[#GPT (GUID Partition Table)|GPT]]
- [[#MBR (Master Boot Record)|MBR]]

>Note that whenever you create a new partition, you will be overwriting any saved data that was originally there. This data, after partitioning, is unrecoverable.

### GPT (GUID Partition Table)

>More from [wikipedia](https://en.wikipedia.org/wiki/GUID_Partition_Table).

This is the latest partition format standard wherein each partition you create gets a globally unique identifier (GUID) assigned to it.

- requires a [[The BIOS#Universal Extensible Firmware Interface (UEFI)|UEFI BIOS]]
- can have up to 128 partitions
- supports a maximum partition size of over 9 billion TB
	- the maximum partition size for Windows is 256 TB
- there is no such thing as extended partitions nor logical drives in GPT

### MBR (Master Boot Record)

>More from [wikipedia](https://en.wikipedia.org/wiki/Master_boot_record).

This is the old standard of partitioning and is still somewhat used, however I'm sure that it's mainly only used with older operating systems or virtual machines.

There are two partition types:

- primary
	- these are bootable partitions, with a maximum of 4 per disk
	- one of these primary partitions can be marked as "active" (meaning that the computer will automatically boot from the active partition)
- [extended](https://en.wikipedia.org/wiki/Extended_boot_record) (optional)
	- used for extending the maximum number of partitions
	- the extended partition can be broken up into smaller logical partitions
	- logical partitions are not bootable
