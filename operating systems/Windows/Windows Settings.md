Tags: [#os #windows]
Shortcut: `WINDOWS + I`

# Windows Settings

This is the Windows Settings app, the newer, sleeker version of [[Control Panel|control panel]] with almost the same functionality but easier to use for newer users and boomers (I think this has less in-depth control and features).

Here's a list of built-in applets to manage various settings of your machine:

- [[#Time & Language|time & language]]
- [[#Update & Security|update & security]]
- [[#Personalization|personalization]]
- [[#Apps|apps]]
- [[#Privacy|privacy]]
- [[#System|system]]
- [[#Devices|devices]]
- [[#Network & Internet|network & internet]]
- [[#Gaming|gaming]]
- [[#Accounts|accounts]]

## Time & Language

Here you can set:

- set the time manually or automagically
- set the timezone manually or automagically
- synchronize your clock ([[Active Directory|active directory]] is apparently very sensitive to clock time with a 5 minute tolerance)
- set the country or region
- set the language of your machine
	- along with adding various keyboards for different languages
	- set the default language of certain options:
		- display, apps, regional format, keyboard, speech recognition
- manage speech recognition and narrator settings

>I remember there being a virus made by Russian hacking group that would deactivate itself if you had a Russian keyboard installed.
>This is most likely to avoid being targeted by the Russian authorities.

## Update & Security

Here you can:

- check for updates for Windows
- update your Windows version
	- you can customize the time of day when Windows can and cannot try and update itself
	- you should be a real man and just disable updates
- customize security options (e.g., manage Windows Defender)
- create and restore from backup
- allow downloads from other Windows PCs (actually a pretty cool feature ngl)
- recovery options
	- reset
	- advanced startup to change firmware settings, startup settings or restore from a Windows image
- Windows product activation
	- if you either bought Windows or you found some random activation key online
- developer features
	- file explorer options
	- install apps from any source (not *from* source)
- find my device feature
	- similar to "Find my iPhone"
- the Windows Insider Program
	- I think this is to get features earlier and to beta-test them for Microsoft

## Personalization

Here you can:

- change the wallpaper
- change fonts
- change colors
- customize the taskbar
	- but you can't remove any of the stupid applets like news or weather because fuck you
	- the taskbar remains on the bottom with applets justified to the left as God intended
- other stuff

>I don't think that this section is overly important to the a+ certificate.

## Apps

This is where you manage your apps:

- configure, repair and uninstall programs
- change the default handler for files of a certain extension
	- choose default apps by extension
		- Windows doesn't use the magic bytes like Linux does
	- choose default apps by protocol
		- sadly you cannot add any protocols
- change startup apps (this can also be done from [[Task Manager]])
- a section to download maps for when you're offline
- video playback for the built-in Windows video player

## Privacy

Here you can manage settings for:

- let apps use your own advertising ID
	- I don't know why you'd ever willingly turn this on
- allow or deny websites to use your locally set language to load language/region specific content to your browser
- toggle online speech recognition on or off
- toggle diagnostics and telemetry
- allow and deny apps to use
	- location
	- camera
	- micropone
	- voice activation
	- notifications
	- account info
	- contacts
	- calendar
	- phone calls
	- call history
	- email
	- tasks
	- messaging
	- radios (apparently)
	- other devices
	- background apps
	- app diagnostics
	- automatic file downloads
	- documents
	- pictures
	- videos
	- file system

## System

Here you can:

- choose display settings
	- resolution, font size, app icon size, etc.
- sound
	- input and output devices along with their volumes
- notifications
	- what is and is not allowed to create a push notification
- focus assist
	- depending on what you're doing or the time of day you can control what apps are allowed to create a push notification
- power and sleep
	- basically, when should the screen turn off and when should the PC sleep
- tablet settings
- storage
	- cleanup temporary files and apps you don't really use
- multitasking
	- window snap properties
	- timeline (no idea what this is)
	- how `ALT + TAB` behaves
	- virtual desktop behavior
- projecting to this PC
	- a bunch of authentication settings
- shared experiences
	- apps that have been managed by a third-party such as work or school
	- enable and disable local sharing across devices
- clipboard
	- you can turn a setting on that if you hit `WINDOWS + V` you can pull up your clipboard history
- RDP settings
	- enable and disable RDP
- the about section 
	- displays a bunch of information about your machine

## Devices

Here's where you manage bluetooth, printers & scanners devices and:

- mouse settings
	- choosing your primary action button
	- cursor speed
- typing
	- this is basically auto-complete and auto-grammar features
- pen & Windows Ink
	- hand writing features and fonts
- AutoPlay
	- controls what to do when you insert a USB or memory card
- USB
	- notifications for any errors or a slow charge over USB

## Network & Internet

- status
	- see the status of your internet connection
- Wi-Fi
	- see your list of memorized networks
- ethernet
	- see your ethernet connection settings
- dial-up
	- manage your dial-up connections
- VPN
	- manage your VPN clients and connections
- airplane mode
	- enable or disable airplane mode
	- airplane mode just disables almost all wireless features such as Wi-Fi and bluetooth
- mobile hotspot
	- you can turn your PC into a hotspot
	- something I didn't know about
- proxy
	- add and or remove a proxy

## Gaming

This is primarily for Xbox features, here you can manage:

- the Xbox game bar
	- enable and disable the game bar
	- also a bunch of keyboard shortcuts
- captures
	- for recording your sessions and settings
- game mode
	- enables and disables optimization for gaming
- Xbox networking
	- this just tells you the connection and type you have to Xbox servers

## Accounts

Here's some high level options for:

- viewing your account info
- registered emails and accounts for various apps
- sign-in methods
	- authentication methods
		- Windows Hello Face (face recognition)
		- Windows Hello Fingerprint (biometrics)
		- Windows Hello Pin
		- security key
			- instead of a password, insert a USB to authenticate and log in
		- password (a regular old password)
		- picture password
			- choose the correct picture out of a list of pictures
	- require sign-in boolean
	- dynamic lock
		- if you have a paired device and go out of range of this computer, lock the device
	- restart apps
		- save restartable apps when you sign out and restart them after sign in
	- privacy
		- show account details on sign-in screen
- access work or school
	- a list of accounts for work or school
- family & other users
	- I think this is cloud storage for a family that uses one device
- sync your settings
	- backup settings to the cloud
