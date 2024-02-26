---
tags:
  - hardware
---
# The Basic Input/Output System (BIOS)

BIOS stands for "Basic Input/Output System" and it is the first thing to run on a computer when it starts up. The BIOS is software that is built into the [[The Motherboard|motherboard]] that initializes the computer's peripherals.

After the BIOS initializes the computer's peripherals and does a [[#Power On Self Test (POST)|POST]], it will then searches for a boot device. The boot device is typically stores on a [[HDD|hard drive]]. The boot device can either be software or an operating system.

The BIOS is stored within a chip on the [[The Motherboard|motherboard]] and is powered (to retain data) by the CMOS battery.

Using the BIOS you can change things such as;

- the date and time
- virtualization
- integrated peripherals such as
	- [[Sound Port|sound]]
	- [[Ethernet Port|network]]
	- [[USB|the USB controller]]
	- [[Video Port|video]]
- [[CPU|CPU]]
	- clock speed
	- voltage

The BIOS can monitor the [[CPU|CPU]] temperature and if the CPU [[Fans|fan]] is running. The BIOS can actually stop the boot of a computer if it detects the fan isn't running. It does this to prevent damage happening from the computer.

The BIOS can detect if the computer case has been opened and will alert the user.

## Universal Extensible Firmware Interface (UEFI)

This is the modern version of the BIOS and is an overall improvement of the previous implementation. One of the new features is an improved graphical interface that can support animations whilst the older one resembles the windows blue screen of death (BSOD).

UEFI can utilize the mouse as well as opposed to the BIOS' keyboard only. Another feature is secure boot, this is to protect the computer from digitally unsigned drivers and malicious software such as rootkits.

## Boot Priority

When you turn on a computer, the computer does a power on self test ([[#Power On Self Test (POST)|POST]]). This ensure that all the vital components are working, after this test the BIOS will then search for something to boot from (usually an operating system).

You can also boot from a [[USB Stick|USB]], [[CD-ROM|CD]] or even a [[The Floppy Drive|floppy disk]] as long as they have the proper boot files on them. These boot devices are stored in a list in the BIOS and the BIOS will check each one for something to boot from. The previously mentioned list and be changed.

## Power On Self Test (POST)

To know if the POST worked, the computer will produce a short beeping noise to audibly let the user know that it is running properly. You will also know if the computer boots up into the operating system you're expecting.

If there aren't any beeps or if there are multiple, this indicates that the POST failed and that there is something wrong with the computer.

For example if there are three long beeps, this could mean that something is wrong with they keyboard module. You can refer to the manufacturer's documentation to see the list of beep codes.

## Functions

- It is firmware software that establishes the abse behavior of a computer
- It sets the hardware configuration of the computer
- It tells the computer what hardware to initialize and in what order (a.k.a. priority)
	- some of these devices include
		- keyboard
		- mouse
		- [[Graphics Card|video card]]
		- [[CD-ROM|optical drives]]
- The BIOS points out to the PC the files which are needed in order to boot up the operating system

## Properties

- The BIOS is stored in [[RAM Types#Non-Volatile RAM (NVRAM)|nonvolatile RAM (NVRAM)]]
- It is designed and coded for a specific [[The Motherboard|motherboard]]
- BIOS updates can add functionality to a system that wasn't originally present

## How do I access the BIOS?

Usually, when booting up a computer there is a window of time that you can press a specific key such as an F-key or another special key to open up the BIOS menu.

## Why would I need to access the BIOS?

Sometimes when you add a new component to a PC you'll need to update some of the settings within the BIOS to work properly with the new hardware.

Accessing the BIOS might also be important with system recovery.

## How do I update the BIOS?

You'll need to download the update (which is usually a .exe file) and then run it to update the BIOS. Sometimes you'll need to swap operating systems in case the BIOS update file can't run on your system (e.g., you've downloaded a .exe file on some Linux distribution).

If the update fails or something along those lines, this is very bad since the BIOS is required for the computer to update. If the update fails and the BIOS is now corrupted, you'll either need to flash a valid copy of the BIOS to some chip on the [[The Motherboard|motherboard]] or you will need to buy another motherboard.
