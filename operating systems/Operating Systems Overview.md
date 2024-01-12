Tags: [#os]

# Operating Systems Overview

The main goal of an operating system is to be the tool which the user requires in order to complete their task.

Your average user will require the following:

- a graphical desktop
- a way to retrieve, store, rename and organize files in a hierarchical structure
- a place to store files without them being lost or corrupted
- a way to access the internet or a network
- some form of entertainment
	- this is usually either YouTube (internet) or a video game
- an email client
- tools to help them create:
	- spreadsheets
	- documents
	- slideshows
- a calculator
- some method to configure their operating system (in the visual or behavioral sense)
- input and output support
	- keyboards and mice
	- external storage drives
- printer support

More advanced users might require features such as:

- low-level access to both software and hardware components such as the network card, the kernel, drivers, etc.
	- including low-level configuration
- a scripting language to interface with the operating system
- tools to view networking devices
- packet sniffers
- programming language build tools
- specific architectures
- additional hardware/driver support for third-party systems such as:
	- complex sound systems
	- drawing tablets
	- cameras

IT administrators would require:

- tools to remotely push and pull networking configuration to computers, routers, switches or any other networking device (think [[Active Directory]])

## List of Operating Systems

Here are the most common operating systems available to the public:

- [[#Windows|Windows]]
- [[#Linux|Linux]]
- Apple
	- [[#macOS|macOS]]
	- [[#iOS|iOS]]
	- [[#iPadOS|iPadOS]]
- [[#ChromeOS|ChomeOS]]
- [[#Google Android|Android]]
- [[#Vendor Specific Software|Vendor Specific Software]]

## Windows

This is by far the most common operating system used in the market for consumers, prosumers and corporations and has the largest market share.

- advantages
	- large industry and tech support
	- large software support; most applications and video games run on Windows
- disadvantages
	- prone to hacks and security exploits
	- large hardware support can create challenging integration exercises
	- odds are you paid for Windows
	- absolutely proprietary
	- spyware is probably installed on your PC by default along with a couple three-letter agency backdoors built-in
	- it's Windows

## Linux

This is *like* Unix, not *is* Unix. There are probably thousands of distributions at this point, most of which are based on a singular architecture/flavor of Linux.

- advantages
	- it's absolutely free
	- everything on your computer is open-source
		- meaning that you can change it at any time but more importantly you can see what it does and how it behaves
	- works on a large variety of hardware (OpenBSD is a great example)
	- a very passionate and active user community
- disadvantages
	- limited driver support, especially with laptops
		- looking at you Nvidia
	- limited support options
	- somewhat limited application support, especially for gaming
		- if something only runs on [[#Windows|Windows]], your best bet is either find something else or find a way to emulate it, like Wine
	- requires knowledge of computers beyond the surface level, usually a familiarity with programming

>This is the single best operating system.

## Apple

### macOS

This is like a proprietary version of [[#Linux|Linux]] (I believe based on Debian) for the average consumer. It's almost like the Windows version of Linux targeted for consumers.

It's quite easy to use and has some nice features to make it a good daily driver. The main feature of macOS is its integration into the Apple software and hardware ecosystem.

- advantages
	- easy to use
	- relatively fewer security concerns
	- it's very similar to standard Linux and comes with all the classic Linux utilities
- disadvantages
	- will only run on Apple hardware
	- less industry/software support than the Windows platform
	- way too costly compared to what you get
		- Apple is not cheap and they love to price gouge you for repairs or anything Apple related really

>Keep in mind that macOS has its own executable format, the `.app` extension. I don't think native Linux programs (ELF files) will work due to either libraries being unavailable or a matter of file format.

>Any computer that isn't an Apple product that's running macOS is called a "Hackintosh".

### iOS

This is the operating system that runs on iPhones. This OS is based on Unix and is absolutely proprietary. This OS is exclusive to iPhones and will not run on anything else.

>iOS apps are developed with iOS SDK on [[#macOS|macOS]] with all apps having to be approved by Apple before they get released onto the Apple App Store.

### iPadOS

This is Apple's OS for iPads, which is a variant of iOS for iPhones. The main features that make this OS different from iOS are:

- a desktop browser version of Safari
- able to be used as a second monitor (sidecar)
- keyboard support
- multitasking, able to run multiple apps simultaneously

## ChromeOS

This is basically laptop: cloud edition. This is Google's operating system which is based on the [[#Linux|Linux]] kernel (as so many thing are). This centers around the Chrome web browser.

They are relatively cheap and come from numerous manufacturers, however, they rely on the cloud and **must** have an internet connection.

## Google Android

This is an open-source operating system based on [[#Linux|Linux]] but it's really semi-open-source because when this OS gets installed onto a phone by any manufacturer, it comes prepackaged with closed-source Google apps which are innately spooky.

However, the main driver is open-source and that's what mainly matters since you can remove all the Google utilities from your phone.

>Android apps can be developed on [[#Windows|Windows]], [[#macOS|macOS]], [[#Linux|Linux]] with the Android SDK. Apps are available from the Google Play store but can be side-loaded or installed via. `.apk` files.
>Apps are also available from third-party sites such as the Amazon Appstore.

## Vendor Specific Software

Vendor specific software is mainly for things such as routers, switches, mainly any networking equipment along or other devices.

The support of this software and or hardware is dependent on the vendor that supplies it, it could be either really good and setup to be maintained for a long time or shitty and the end of life will be three years after launch.

One thing to note is the application compatibility and the operating system compatibility. If your workplace uses macOS for example but the piece of software or hardware you need only runs on Windows or has a driver only for Windows, then you're kind of out of luck.

>Webapps should be immune to this rule since they (should) only rely on the browser and not the hardware.
>E.g., it should not matter if an Apple, Windows or Linux computer accesses a Shaw or Broadcom router from their browser.
