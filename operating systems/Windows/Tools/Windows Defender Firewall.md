---
tags:
  - os
  - windows
  - networking
---
# Windows Defender Firewall

This is the built-in firewall for Windows and comes shipped with every single [[Windows Editions|edition]]. You can disable this firewall manually by opening [[Control Panel|control panel]] and clicking the "Windows Defender Firewall" applet.

Just like [[Windows Network Technologies#Network Privacy|network profiles]], Windows Defender has a public and private option for networks where you can automatically enable/disable the firewall when connected to a public or private network.

>Disabling Windows Defender Firewall requires elevated permissions.

You can also block all incoming connections, including those in the list of the allowed apps. Any app that wants to do anything networking related, it must first ask the firewall for permission.

## Configuring Firewall Exceptions

![[Pasted image 20230825153245.png]]

Windows Defender Firewall is a [[Firewall#Host Based Firewalls|host-based firewall]], meaning that it knows every single application that's on your computer and has a rule of whether or not any given app installed on your PC can transmit data over the network.

In the "Allowed Apps" section of this applet, you can configure which applications are allowed on both either profile of Windows Defender.

>You can manage each application more in-depth via. going into the "Advanced Options" section of the applet.
>Configure options such as: port number, protocol, the targeted .exe file, a list of IP addresses both local and remote, connections from certain computers, etc.

## Creating Firewall Exceptions

In the "Advanced Options" section, you can create new rules with the following properties:

- rule type
	- one of: program, [[Networking Ports|port]], a predefined rule or a new custom rule
- protocols and ports
	- either [[TCP|TCP]] or [[UDP|UDP]] along
	- all ports or a list of ports
- action
	- one of: allow the connection, allow if secure or block
- profile
	- when the rule applies:
		- domain - a corporate domain
		- private - the private profile
		- public - the public profile
- name
	- the name of this new firewall exception and an optional description

