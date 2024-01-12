---
tags:
  - os
  - windows
---

# Windows Features

This note is mainly about the management features that Windows offers for controlling and managing huge networks of Windows machines in a corporate environment.

Windows includes security features for a corporate setting along with including various *productivity apps* for users such as Microsoft Word, PowerPoint, Excel, etc.

Finally, Windows includes tools for managing files and access for large companies that have various physical locations which can be miles apart.

## Domain Services

This is [[Active Directory|active directory]], basically a huge database full of information such as:

- users
	- name
	- email
	- username
	- password
- devices
- printers
- permissions

This also has a distributed architecture, for example, instead of having one monolithic database at a single location, instead have a database for each corporate setting with their own printers, scanners, computers, users, etc.

>Finally, this also doubles as authentication wherein when you log into a computer, the authentication service is the active directory server.

## Network Device Management

There are two main ways to manage a network of devices:

- Windows Workgroups
	- each device is standalone with no central authentication service nor centralized database that contains information about every device on a network
- Windows Domain
	- this is for a bigger setting comprised of thousands of devices across many networks

## Desktop Styling

Pretty much this:

- work
	- this is a standard, non-personalized, depressing workstation with nothing much to offer
	- not much customization and extremely generic
- home
	- lots of customization and flexibility
	- wallpapers, colors, UI sizing, etc.

## RDP

>For information about the protocol, see [[RDP]].

This service allows for people to log onto computers via. the network, removing the need to be physically at the target computer. This is similar to [[SSH|SSH]], however, instead of being given just a terminal you are provided with a full graphical interface.

In order to connect to a computer via. RDP, you must use an RDP Client, which is available for almost any operating system (Windows, Linux, macOS). The target machine must be running the Remote Desktop Service, this is what allows the RDP connection to happen.

>Note that the Remote Desktop Service isn't available in Windows 10 Home.
>Also, RDP *was* a Windows specific protocol. It is primarily used for Windows, however you can install an RDP service on a Linux machine.

## BitLocker and EFS

Both BitLocker and EFS (Encrypting File System) encrypt files on your storage drive, however:

- EFS protects individual files and folders, and is also built-in to the NTFS file system
- BitLocker provides FDE (full disk encryption) and encrypts everything on the drive
	- including the operating system

Using BitLocker, the only way to access your computer is by entering the password to decrypt the drive.

>However, I'm sure that there's a way around this. The NSA has probably already figured that out.

As far as consumer grade software goes, it's not bad. This is good for security and data confidentiality.

>Disk encryption won't really matter if you install some sort of virus on the machine while it's decrypted and running.

## Group Policy Editor

This is a tool to manage [[Active Directory|Active Directory]], you really won't be using this outside of a corporate environment where you need to be able to manage hundreds or thousands of accounts.

>See article about the [[Group Policy Editor]] utility.
