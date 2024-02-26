---
tags:
  - security
  - networking
---
# Securing a SOHO Network

- update and upgrade the firmware of your router
- allow and block IP addresses or URLs
- put your router in a secure room or somewhere that is secure so that people can't physically access it
- it's a good idea to configure your DHCP server to do "address reservations" so that a user gets the same IP address every time they connect to the network, also known as:
    - static DHCP assignment
    - static DHCP
    - static assignment
    - IP reservation
- it's sometimes a good idea to have a static IP associated with your router, but odds are you will have to buy one from your ISP

## Things to Disable

It's generally good practice to disable Universal Plug and Play (UPnP) because it automatically port forwards for you on an application by application basis. In turn, what could happen is malware can use the UPnP feature to establish a RAT or a backdoor into your network.

If you want to use UPnP, you should consider a [[#Screened Subnet]].

Disable the guest network, random people shouldn't be connecting to your internet (unless you want them to).

In a conference room, odds are there will be exposed ethernet ports in a table or in the room for the business people to talk about money and laundry. The connectivity of these ports should be togglable so that random people can't just walk into an empty conference room and have full access to your network.

>This is somewhat easier said than done but an idea is to have them on a separate subnet or just enable and disable the switches that are responsible for dealing with them.

## Things to Change

Always chance the default username, password of your network and router. It's very common for attackers to try and hack your router by using the default username and password.

It would also help if you changed the default name of your router. By changing your SSID from LINKSYS or NETGEAR, you make it harder for people to guess what kind of router or access point you have.

>See this [website](https://www.routerpasswords.com).

## Screened Subnet

This is a subnet that is not associated with your internal network but is still communicating with your firewall. It's like a playground for resources from the internet to communicate with and is isolated from your home network.

## Network Encryption

There's a couple use cases here:

For an environment like a hotel or a coffee shop, it would make sense to use an open system connection where there is no username nor password to be entered.

For something like a home or maybe a small business, using WPA2/3-Personal/PSK would be a good choice as people only have to remember a password.

For something like an office or an enterprise environment, using WPA2/3-Enterprise or WPA2/3-802.1X is a good idea because you would have to change the PSK for each person that leaves. However, because of this you will have to setup some form of authentication server like [[RADIUS]] or [[LDAP]].

Sometimes, there will be many access points that use up their own frequencies to transmit locally, therefore for a new network, you'll have to use frequencies that are open/not being used. You can buy access points that will automatically find good, unused frequencies to use.
