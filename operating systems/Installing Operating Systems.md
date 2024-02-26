---
tags:
  - os
---
# Installing Operating Systems

To actually install something to make your computer function, you must first have something for the computer to boot from. This could be:

- a hard drive
	- [[HDD]]
	- [[SSD]]
	- [[External Hard Drive|external drive]]
- a [[USB Stick|USB drive]]
- a [[CD-ROM|CD]]
- an [[SD Card|SD card]]
- Preboot eXecution Environment (PXE or "Pixie")
	- this is a remote network installation
	- your computer must support PXE for this to work
- Internet-based installation
	- this includes:
		- downloading software from a Linux package server
		- a macOS recovery installation
		- Windows updates

Note that in order for the computer to boot, it must be able to detect a *bootable device* on the media.

>I believe this checking the first 512 bytes of the media and seeing if there is something there to execute, like an instruction pointer or something.

You technically do not require an external media device to boot from, it is possible to install an OS from your one and only hard drive. However, you still require something to boot from. The main issue here is getting an operating system onto your drive, this most likely requires another computer.

## Types of Installations

>Note that operating systems get installed into [[Device Partitioning|partitions]] on a storage device.

There are several methods of installing an operating system, they are:

- in-place upgrade
	- this is where you just upgrade the operating system and NOT erase any install programs or files on your computer
	- e.g., upgrade from Windows 7 to Windows 10
- recovery partition
	- this is a handy tool for recovering your OS, this is a separate partition on your storage drive that contains a bunch of installation tools so you don't have to figure out what or where your old installation tool went
- clean install
	- here, you are wiping the computer clean, not caring about what's on it, you just need the computer and not whatever is inside of it
- image deployment
	- this is very useful for a corporate environment wherein everyone gets the same installation on their computer this includes:
		- configuration settings
		- installed applications
		- authentication/tokens?
	- this is a quick process and if something goes wrong you can simply just reflash the image onto the computer to make it as good as new (software wise, this will not fix any hardware issues)
- repair installation
	- this is where you install the same OS that's currently running on the computer, trying to fix any issues that have happened
	- I'm not sure if Linux has this, however Windows certainly does
	- many application installers have this feature
	- this is kinda like a factory reset for phones however you keep your files
- remote network installtaion
	- here you are installing an operating system from a local server on the network or a shared drive
	- alternatively, you could install an OS from the internet

>Sometimes during an install, certain pieces of hardware won't work due to needing special drivers that haven't been installed yet.
>Some operating system installers come with a feature to install drivers during the install process to allow the install to be completed successfully.
