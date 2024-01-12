Tags: [#os #windows #networking]

# Windows Network Technologies

This note is about various networking technologies that you can use on your Windows machine.

## Shared Resources

This is a way of sharing folders, printers and scanners from your machine to other Windows machines on the network.

>To browse the local network for shares, you must enable "Network Discovery" in:
>Control Panel, Network and Sharing Center, Advanced Sharing Settings.
>
>To enable file and printer sharing you must enable "File and Printer Sharing" in:
>Control Panel, Network and Sharing Center, Advanced Sharing Settings.

### Sharing Folders

Simply right click any folder from File Explorer, go to "Properties", finally the "Sharing" tab.

Each share contains:

- a name
	- if your name ends with a "$", then it is hidden from the network
	- however, it is still present on the network and you can connect to it if you know what the name is
- a path to the folder you want to share
- the type (this is Windows by default)
- \# Client Connections
	- this isn't set by a user, but rather how many computers are connected to this share
- a description of the share

>You can see the list of all shares by going into:
>Administrative Tools, Computer Management, Shared Folders, Shares.

### Sharing Printers

You can share printers and scanners as well. Simply:

1. open up [[Windows Settings|the settings app]]
2. go to "Printers & Scanners"
3. hit "Manage" on the printer/scanner you want to share
4. go to "Printer Properties"
5. finally, go to the "Sharing" tab

This will create a network share for your printer/scanner and is available on the network.

>You don't need to go through this exact process, as long as you can get to "Printer Properties" then you're fine.

## Mapping Network Drives

Provided that there are shares on the network, you can mount a share to Windows via. the "Map network drive" option in the "This PC" tab.

For any network share that you want to mount, it requires:

- a drive letter such as D:\\ or E:\\ for your local machine
- a location
	- a string of format `\\[IP|hostname]\[share name]`
- extra credentials

You have an option for Windows to automatically reconnect to the share on log-in.

>You can also use the command line for this:
>`net use [drive letter]: "\\[IP|hostname]\[share name]"`

### Mapping Printers

In order to add a shared printer:

1. open up [[Windows Settings|the settings app]]
2. go to "Printers & Scanners"
3. hit "Add a printer or scanner"
4. wait for "The printer I want isn't listed" and click it
5. type in the resource name for the printer
	1. format `\\[IP|hostname]\[share name]`
6. and then add it

### Removing Mapped Drives

In File Explorer, go to the "This PC" tab, click the downwards facing arrow on "Map network drive" widget and click "Disconnect network drive".

## Proxy Settings

To manage proxy settings:

1. open up [[Windows Settings|the settings app]]
2. go to "Network & Internet"
3. go to the "Proxy" tab

Here, you can automatically detect the settings of the proxy, or, you can manually configure the proxy.

## Network Privacy

This is a decent feature. Basically, if Windows thinks you're connected to a public network e.g., a coffee shop, airport, etc. it will automatically change the network profile to "Public", meaning that your computer is hidden from other computers and the printer and file sharing features have been turned off.

Conversely, if Windows thinks that you're on a private network (basically a home network), it will change your network profile to "Private", showing your computer to all other computers on the network and will enable the file and printer sharing features.

>You can change this profile at any time by accessing:
>Settings, Network & Internet, Status, "Change connection properties" and choosing the Network profile that you want.

## Metered Connections

Here you can enable a metered connection wherein you can set how many megabytes or gigabytes the connection is allowed to use per month.

Metered connections are very useful when:

- you have slow network links
- you have limited bandwidth
- or you have usage-based billing

Here's what the screen should look like (under Network & Internet, Status):

![[network_usage_example.png]]

- "Properties" to show all the connection settings and enable/disable a metered connection.
- "Data usage" will show you how much bandwidth each application has used over the last 30 days

>You don't need to enable a metered connection to view the bandwidth consumption.
>For some reason, Discord has used over 170 GB in the past 30 days.

You can set a data limit of:

- monthly
- one time
- unlimited
- the date of the month at which this resets
- the limit in megabytes or gigabytes

If you enabled a metered connection and have set a monthly data limit, certain features such as OneDrive and Windows Updates, will pause and you will have to manually reenable them if you want them to work.
