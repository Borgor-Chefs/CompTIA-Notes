---
tags:
  - os
  - macos
---
# macOS Overview

Here's some features of macOS.

>See [[XProtect]]

## File Types

>Something to note, Apple doesn't really use MIME types, Apple uses a [[Uniform Type Identifier|Uniform Type Identifier]] which is a fully qualified string to describe the actual type of a file.

- Apple Disk Image
	- extensions: `.dmg, .smi, .img`
	- MIME type: `application/x-apple-diskimage`
	- Windows equivalent: `.iso`
	- this is usually an application or some kind compressed into a `.dmg` file, this can be mounted as a drive in Finder where you can see the contents
- Installer Package
	- extensions: `.pkg`
	- MIME type: ?
	- Windows equivalent: kinda like a `.exe` setup/installer for macOS
	- this is commonly used to distribute software and runs an installer script to actually install the software
- Application Bundle (see more [here](https://en.wikipedia.org/wiki/Bundle_(macOS)))
	- extensions: `.app`
	- MIME type: ?
	- Windows equivalent: similar to a `.exe` application but more like a Java `.jar` file
	- this is the `.exe` equivalent for Windows, however it is more advanced, it's more like a `.jar` file where you can inspect all of the files and other content inside of it (very cool)

## The Apple App Store

This is a centralized place to install Apple verified applications onto your computer. This is kinda like a GUI package manager for Apple.

>Another very cool feature Windows was too late to adopt.
>Also Windows users commonly go to sketchy websites to install their applications, I do this periodically too lol.

## Uninstalling Programs

Since all programs are `.app` extensions, you can simply move them into the Trash bin and hit the delete button. Very simple and easy.

Some programs include their own uninstaller, this uninstaller is found within their Application folder.

## Apple ID and Corporate Restrictions

Apple requires you to connect your Apple ID to your computer to actually install applications from the App Store, this is the same as any iPhone, iPod or iPad that you use. This is used as purchase verification among other things and to associate you with your (totally not sold or spied on) personal data.

However, in the corporate setting, Apple can integrate with [[Active Directory|active directory]] using Apple Business Manager. On any piece of Apple hardware given to you by a company, it will have a "Managed Apple ID" which is your Apple ID for the business.

It can connect with an existing Mobile Device Manager (MDM), so your corporate computer can connect and view your iPhone, iPad or any other Apple device you've connected.

Finally, using Apple Business Manager, IT admins can control and distribute applications and data to selected users.

## Backups

You can create backups of your system with the Apple Time Machine application. Where you can create backups every:

- hour
- day
- week

Where the oldest backups are deleted when your system becomes full.
