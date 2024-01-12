Tags: [#os #windows]

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
