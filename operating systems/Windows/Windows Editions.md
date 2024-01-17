---
tags:
  - os
  - windows
---
# Windows 10

Windows 10 was released on July 29, 2015 (wow that's a long time ago) and is a single platform that can run on desktops, laptops, tablets, phones and all-in-one devices.

Windows 10 also has ongoing updates with more than 12 different released versions.

## Hardware Requirements

Here are the hardware requirements for Windows 10:

| |32-bit (x86) Windows 10|64-bit (x64) Windows 10|
|-|-|-|
|CPU|1 GHz or faster|Same|
|Memory|1 GB RAM|2 GB RAM|
|Storage|32 GB or more|Same|
|Video|Microsoft DirectX 9 graphics device with WDDM driver, minimum resolution of 800 by 600|Same|

>Windows Display Driver Model (WDDM)
>Taken from [here](https://www.microsoft.com/en-us/windows/windows-10-specifications).

## Summarized Features

Here's a table of supported features by Windows 10 edition:

|Windows 10 Edition|Domain Access|BitLocker|Remote Desktop|Active Directory|Max x86 RAM|Max x64 RAM|
|-|-|-|-|-|-|-|
|Home|No|No|Client Only|No|4 GB|128 GB|
|Pro|Yes|Yes|Client and Host|Yes|4 GB|2 TB|
|Pro for Workstations|Yes|Yes|Client and Host|Yes|4 GB|6 TB|
|Enterprise|Yes|Yes|Client and Host|Yes|4 GB|6 TB|

>I'm pretty sure most of these features are turned off via. software locks which get enabled/disabled depending on the product key that you enter.
>This would make deployment and management of the operating system much easier.

## Windows 10 Home

This is the standard consumer-grade Windows 10 distribution. It was integration with your Microsoft account with Microsoft OneDrive features built into the operating system.

Comes with the standard Windows Defender anti-virus and Cortana.

## Windows 10 Pro

This is more of a business version of Windows that comes with some additional features:

- RDP hosting
- BitLocker
- Active Directory

### Windows 10 Pro for Workstations

This is an extension of the Windows 10 Pro edition for high-end and high-performance desktops.

This edition supports up to 4 physical CPUs (honestly not sure why you'd have more than one CPU at a given time) along with supporting up to 6 TB of RAM.

Finally, it also ships with support for ReFS (Resilient File System) which is the same FS type as Windows Server.

## Windows 10 Enterprise

This was built for large enterprise environments e.g., large implementations and management of potentially hundreds or more Windows 10 deployments in a company setting.

With the scope of the implementation, Windows 10 Enterprise also comes with features to help the implementer to manage each system:

- AppLocker
	- this controls what applications can and cannot run within the corporate setting
- BranchCache
	- this is remote site file caching so that each file doesn't have to be pulled across a potentially slow internet connection, instead it is cached on a local remote server

You also have granular user experience (UX) control over the operating system. This is useful for things like kiosks at malls to customize how they display things and their layout.
