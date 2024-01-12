---
tags:
  - os
  - windows
---
# Upgrading Windows

This doesn't really show any new concepts but is rather more of a checklist of decisions to make and actions to complete when you're upgrading Windows to a newer version (mind you with [[Operating Systems Overview#Linux|Linux]] it just works$^\text{TM}$).

Here's a list of things to think about when upgrading:

- [[#Upgrade V.s. Install|upgrade v.s. install]]
- [[#Preparing the Boot Device|boot device]]
- [[#OS Requirements|OS requirements]]
- [[#Hardware Compatibility|hardware compatibility]]
- [[#Post-Installation Tasks|post-installation tasks]]

## Upgrade V.s. Install

Upgrading is useful for when you **don't** want to remove all of the data and configuration from the system but merely want to upgrade the operating system. It also saves a bunch of time configuring settings, adding data, installing drivers, etc.

A clean install is useful for when you don't care about the data and configuration of your system and want to start fresh. This is useful for when something is absolutely fucked and you can't figure out what it is and you don't mind reinstalling everything on your PC, or, something is absolutely fucked and an upgrade won't fix it

>This happened to me, I installed proctoring software for University and the software completely fucked something, my best guess is my registry, so I had to clean install because I didn't make a backup.

Make a backup! It doesn't matter what method you're planning on using, you should always backup your system before you do anything. This is incase something horrible happens and either your clean install/upgrade becomes fucked beyond belief and you either have to do a second clean install or your first clean install because the upgrade failed.

## Preparing the Boot Device

You should be thinking about what is currently stored on your drive and if it means anything or holds any value that you wouldn't want to lose. With an upgrade it won't really matter, with a clean install, the data will get completely wiped from the drive.

Let's say you wanted to upgrade your C: drive from a 256GB HDD to a 1TB SSD, you'd have to perform a clean install on the new SSD. You won't lose any data (because you're not touching the HDD), however I'm not sure if you could cleanly copy any and all configuration settings onto this new drive.

>However, I'm sure that if there's a will, there's a way.

Finally, make a backup! Don't be stupid, especially if you're working on a customer's computer and they need their data intact and not corrupted.

## OS Requirements

You'll need to have a vague idea of what the specs of your computer are, Windows is somewhat unforgiving when it comes to running in low-spec mode (e.g., runs slow and like shit).

- RAM
	- if you're upgrading to a newer version of Windows that requires say 8GB of ram and you have 4GB, either you will have to upgrade your RAM (always a good idea) or you will have to forgo the upgrade
- Disk Space
	- if you don't have enough space to store the operating system and everything else you want, either consider buying another hard drive
		- PC: if you have a PC you can do this very easily
		- laptop: if you need a storage upgrade, you'd have to find a drive that fits the form factor of your laptop's casing to cleanly fit it in, else buy an external hard drive
- CPU
	- your options here if your CPU doesn't meet the requirements of the OS are:
		- overclocking (BIOS setting)
		- CPU upgrade (easy for PC, unsure how to do for laptops)

### Hardware Compatibility

For your hardware, you'd need to think about if your actual computer, in whole, is able to run your operating system. You can check your hardware with Windows 10 Upgrade Checker or PC Health Check for Windows 11.

For example; Windows 11 requires PCs to support Secure Boot TPM 2.0, if you choose to install without having these requirements, Windows might not behave as expected.

>Finally, your CPU could or could not be supported for a newer version of Windows; this could either be because it simply isn't fast enough (which could be solved with overclocking), it is missing a newer more secure instruction (e.g., SSE2, AES or another one) or it is a 32-bit CPU which cannot run a 64-bit version of Windows.

## Post-Installation Tasks

- installing drivers
	- make sure you remember where you originally downloaded your drivers from, usually computer manufacturers have a website where you can download an installer for drivers and it will download and install drivers for you automagically
- license keys
	- remember to have a "totally legit" license key for your Windows 10/11 install
	- or, you should remember or reobtain the license keys for any application which requires it
- installing applications
	- migrating applications from Windows 10 to Windows 11 should be really easy and you shouldn't run into issues, you may run into issues running applications/installers for older versions of Windows since they might call certain applications or require certain DLLs which no longer come shipped with your new version of Windows
	- in this case, you'd be better of either running them in a virtual machine or you can hunt down the missing DLLs
	- for missing applications/Windows binaries, I'm not sure how you'd do this to be honest
