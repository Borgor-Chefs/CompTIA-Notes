---
tags:
  - os
  - windows
---
# Command Line Tools

These are programs that do things from a command line.

- copying
	- `copy`
		- this is basically Linux's `cp` command
	- `xcopy`
		- this is like a mass copy, in Linux speak it is `cp * [destination]`
		- however, if you add the `/s` flag it will recursively copy all subdirectories to the destination
	- `robocopy` (robust copy)
		- this is a better `xcopy`, kinda like a holy grail of file copying
		- this command is fucking massive and quite complex, you can even specify bandwidth limits to file copying, wild
- `sfc`
- `winver`
	- displays information about the Windows install, similar to Linux's `uname`
	- this is useful for troubleshooting, some versions might not have certain patches
- `help [cmd]`
	- this is essentially the `man` command in Linux
	- some commands aren't supported by `help`, you might have to run `[cmd] /?`
		- such as `sfc`
- `shutdown`
	- use `/s` to shutdown, `/r` to restart and `/t [seconds]` to delay the shutdown/restart
		- also `shutdown /a` to cancel the shutdown
	- this shuts down the computer, what did you expect, a flat screen TV?
	- you can also restart the computer instead

## Directory Related

- `cd` (`chdir`)
	- changes to another directory
- `dir`
	- Window's equivalent to `ls`
- `md` (`mkdir`)
	- same as the Linux `mkdir`
- `rd` (`rmdir`)
	- same as the Linux `rmdir`
- drive navigation inputs
	- instead of `cd C:\` you use `C:`

## Disk Management

- `format`
	- this formats a disk on Windows
	- specifically, this wipes and recreates the filesystem on a drive
- `diskpart`
	- a complex disk partitioning tool, similar to `fdisk` or `gparted`
- `chkdsk`
	- returns the status of a disk

## Networking

- `hostname`
	- this displays the name of the machine
- `ipconfig`
	- `ipconfig` displays most IP addresses and other information about the machine from a network POV
	- `ipconfig /all` displays literally everything about your computer from a network POV
- `ping`
	- the generic `ping` utility function
	- `bytes` is the amount of info transferred, `time` is the time it took in total, `TTL` is the amount of "hops" that the packet took to get to the destination e.g., how many servers it went through to get to the desired machine
- `netstat` (network statistics)
	- kinda like a diagnostics tool to view network connections, Wireshark does a better job imo
	- `netstat -a` shows all active connections e.g., inbound and outbound traffic
	- `netstat -b` shows the programs that are making the connections
	- `netstat -n` do *not* resolve hostnames, showing only IP addresses
- `nslookup` (name server lookup)
	- this talks to your local DNS server to resolve the IP address of a given domain
		- e.g., will transform `google.ca` to an IP address
	- this will also display the name of the DNS server, the IP address and the various IPs that correspond to the target domain name
- `net`
	- this is a bunch of windows utilities bundled into a singular command, a lot of commands require some form of group policy
	- `net user`
		- displays all the users on the current system
		- can also be used to reset passwords
	- `net use`
		- can be used to map a drive to a letter on Windows
	- `net view`
		- used to view network resources e.g., printers, scanners, other computers, shares, etc.
			- I think a share is term used to describe a machine running on your network
		- I think this can only be used if you have a workgroup setup (e.g., group policy shit)
- `pathping`
	- `pathping -n` will only display IP addresses
	- this combines the functionality of `ping` and `tracert`
	- this command operates in phases
		- phase one runs a `tracert` to build a map of devices
		- phase two measures the round trip time and packet loss at each hop
- `tracert`
	- `tracert -d` prevents the resolution of IP addresses to domain names
	- this is a good way to figure out of your IP tables configuration works as intended because you can see what route the packet took to reach its destination
	- this shows the route that a packet took to get to a destination
		- this uses the ICMP protocol and `TTL` to count the hops
		- not all devices will reply with ICMP time exceeded messages, e.g., some firewalls filter out ICMP messages
		- ICMP is a low-priority for many devices, but should be high for DNS servers
	- this program works by sending out $\sum^n_1$ messages up the chain of servers
		- for each server, it will decrement the TTL by one, when it reaches zero, the message gets sent back to the host
		- the program will increment the base TTL until either the maximum hop limit is reached or until the packet reaches the desired destination

`tracert` sample output:

```
C:\Users\XXXXXX>tracert google.ca

Tracing route to google.ca [172.217.14.195]
over a maximum of 30 hops:

  1     7 ms    10 ms    28 ms  xxx.xxx.xxx.xxx
  2    75 ms    55 ms    74 ms  xxx.xxx.xxx.xxx
  3    86 ms    97 ms    76 ms  xxx.xxx.xxx.xxx
  4    81 ms    49 ms    83 ms  xxx.xxx.xxx.xxx
  5    50 ms   156 ms   119 ms  xxx.xxx.xxx.xxx
  6    96 ms   100 ms    62 ms  xxx.xxx.xxx.xxx
  7    63 ms    73 ms    61 ms  xxx.xxx.xxx.xxx
  8   111 ms   122 ms    77 ms  xxx.xxx.xxx.xxx
  9   104 ms   178 ms    58 ms  xxx.xxx.xxx.xxx
 10   168 ms   113 ms    86 ms  xxx.xxx.xxx.xxx
 11    92 ms    41 ms    58 ms  xxx.xxx.xxx.xxx

Trace complete.
```

## Group Policy Management

This is a way to interface with the [[Active Directory|active directory]] service running on your network.

- `gpupdate`
	- this forces a group policy update on a computer or for a user
- `gpresult`
	- this returns the policies for a specific user or to check the changes in policy after an update
