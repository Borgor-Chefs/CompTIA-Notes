Tags: [#os #windows #utility]

# Control Panel

This is a huge collection of "applets" which control various aspects of your Windows machine such as:

- [[#System|system configuration]]
- admin tools
- [[#Network and Sharing Center|network and sharing]]
- security
- user account management
- [[#Devices and Printers|devices and printers]] (Control Panel version)
	- see device manager application [[Device Manager|here]]
- fonts
- mouse
- power options
- RDP connections
- bitlocker
- date and time
- Windows Defender
	- [[#Windows Defender Firewall|the firewall]]
	- the anti-virus
- [[#Programs and Features|programs and features]]
- [[#Internet Options|internet options]]
- [[#Mail|mail]]
- [[#Sound|sound]]
- [[#Indexing Options|indexing options]]
- [[#File Explorer Options|file explorer options]]
- [[#Administrative Tools|administrative tools]]
- [[#Power Options|power options]]
- [[#Ease of Access Center|ease of access options]]

>Some of these applets are standalone programs while others are built into Control Panel.

The reason why Control Panel hasn't been completely removed is that some older installers still call Control Panel directly or make use of things that are basically deprecated but haven't been removed.

>This same reasoning is probably why Windows gets hacked too often, the attack surface is huge.

## Internet Options

This section of the control panel is largely deprecated because it controls the settings of Internet Explorer, which has been deprecated in favor of Microsoft Edge. However, the settings here still get applied to Microsoft Edge.

>On my Windows 10 machine, opening Internet Explorer reroutes to Microsoft Edge.

There is really no reason to use this since most if not more settings are present in Microsoft Edge and configurable right from the browser. This is likely a compatibility feature when migrating from IE to Edge when you upgraded from Windows 7 to a newer version of Windows (e.g., 10 or 11).

However, I think there are some configuration settings which aren't available in modern Edge such as controlling what version of HTTP or TLS you want to use. 

### General

You can set the default homepage, if you want to start from the Home page or from previous tabs on startup, how tabs should be displayed (it should be on the top as God intended), browsing history and some appearance settings.

### Security

You can control the security level of:

- internet
- local intranet
- trusted websites
- restricted websites

You can specifically control:

- ActiveX
- .NET control
- pop-ups
- JavaScript execution
- user authentication
	- such as logging in with your username and password if you want to visit a restricted website
- other miscellaneous options

>Note that these options only take effect *after* you restart your computer.

### Privacy

Here you can control how certain websites react:

- block cookies
- block the location
- block pop-ups
- disable toolbars and extensions when browsing in the Edge equivalent of Incognito mode

### Content

Mainly manages SSL certificates and auto-complete.

### Connections

This is just VPN, LAN and proxy settings.

### Programs

Default browser, add-ons/plugins, default HTML editor, internet programs (e.g., email, discord, steam URLs) and file associations.

### Advanced

More advanced configuration settings.

## Devices and Printers

This is an easier, more user-friendly version of [[Device Manager|device manager]]. This shows speakers, laptops, desktops, printers, multimedia devices, storage, etc.

## Programs and Features

This lists all installed applications where you can:

- see the size on disk
- see the version of the program
- uninstall a program
- repair a program
- turn on and off a Windows feature such as:
	- IE 11
	- .NET framework
	- hyper-visor

## Network and Sharing Center

This shows all network adapters whether they be wired, wireless, virtual, etc, and all their configurations.

## System

On newer versions of Windows, clicking the "System" option in Control Panel will open up the System application where you can view and manage various aspects of your system. Options include:

- Bluetooth and devices
- network & internet
- personalization
- apps
- accounts
- time and language
- gaming
- accessibility
- privacy and security
- Windows update

This new version of the System applet includes other applets which have been "migrated" (it's just a shortcut to open the original executable lmao) such as:

- RDP connections
- device manager
- bit locker
- product key and activation

## Windows Defender Firewall

This allows the user to configure the local firewall rules for the machine.

## Mail

>Note that this icon doesn't appear unless a mail client (such as Microsoft Outlook) is installed.
>Otherwise, this is not an option.

You can control:

- email accounts
- data files e.g., how and where to store emails
- profiles

For each email account you can configure:

- email
- data files
- RSS feeds
- SharePoint lists
- internet calendars
- published calendarrs
- address books

## Sound

This just opens the sound device menu, where you can enable, disable and set the default audio device of your system. Same with recording, also you can control what sounds are produced when certain events happen (e.g., multimedia device connected, error, etc.).

## User Accounts

Here you can manage local accounts on your computer or [[Active Directory|active directory]] accounts that are stored somewhere else. By manage accounts from active directory, I mean that Windows will show your what accounts from active directory are present on your machine and how they are configured.

You can also:

- change password
- change user icon
- manage certificate information for anything that is encrypted

## Device Manager

This is literally just [[Device Manager|device manager]].

## Indexing Options

This is where you can configure Windows to search for applications or files on your machine and where not to look (e.g., parent or subdirectories). This exists because all files and applications are already indexed on your machine to improve search times.

## File Explorer Options

This allows for the configuration of behavior for File Explorer. Options such as:

- on folder open, open in new window or same window
- single or double click to open a file or application
- show recently or frequently used folders in Quick Access
- view hidden files
- use pre-indexed files
- include system directories for searching
- include compressed files

## Administrative Tools

All this does is open up a window from File Explorer with a bunch of shortcuts to various utilities such as:

- [[Event Viewer|event viewer]]
- [[Disk Defragmentation|defrag]]
- [[Registry Edit|registry editor]]

## Power Options

This is how you tell Windows how to act when on certain power modes. Such as:

- parellels v.s. power saver
- balanced v.s. high performance

Also you can control how hibernation, sleeping, idling, what happens when the lid of your laptop closes, etc. You can get very specific such as disabling certain hardware components of your machine when your computer is in a certain power state.

## Ease of Access Center

This is largely for people with disabilities however you can change display, keyboard, mouse and other I/O options such as:

- changing the mouse pointer
- optimize the computer for the blind
- optimize the visual display such that it is easier to use
- setup the computer to be used without a keyboard or mouse
- make the mouse easier to use (whatever this means)
