Tags: [#networking]

# Internet Protocol Address

This is a numeric identifer for computers that want to connect to a network, this is required for a device to communicate on a network.

There are two versions of IP addresses: [[#IPv4|IPv4]] and [[#IPv6|IPv6]].

## Versions

### IPv4

This is a 32-bit numeric address written as four numbers separated by periods. Each segment is called an octet, ranging from 0 to 255 e.g., 127.0.0.1.

There are $2^{32}$ or 4,294,967,296 possible addresses.

>The first octet 127 is reserved for loopback testing.

An IPv4 address consists of two parts: a network address and a host address.

### IPv6

The original architects of networking thought that IPv4 would suffice and that we wouldn't run out of possible IP addresses. They were wrong, so they invented IPv6 which is a 128-bit hexadecimal address, e.g., 76dc:4f59:34cf:71cd:9dc6:89cd:45d6:67a2. Each 4-byte segment is separated by a semicolon.

There are $2^{128}$ or 340,282,366,920,938,463,463,374,607,431,768,211,456 possible addresses.

## Types

There are different types of [[#IPv4|IPv4]] addresses, they are:

- [[#Subnet (Mask)|subnets]]
- [[#Private IP Address|private IPs]]

IPv4 addresses have different classifications and ranges for both public and private addresses.

- [[#Public IPv4 Ranges|public]]
- [[#Private IPv4 Ranges|private]]

### Subnet (Mask)

A subnet is an IPv4 address which dictates what part of the full IPv4 address is for the network and for the host.

![[Pasted image 20230329225554.png]]

Above is how an [[#IPv4|IPv4 address]] is broken down into its two parts: network and host. We use a mask (the network portion of the mask will always be 255) to deduce what part of the IP is for the network and for the host.

The network portion will target devices on a certain network and the host portion will target the actual device.

### Private IP Address

This kind of IP is something that cannot directly access the internet nor is it publically registered ,and this is for good reason. Imagine having a business with 10 computers, you might want 10 public IPs. This isn't a good idea because this could lead to a shortage of addresses.

Instead, if you have one public IP and 10 private IPs, this would reduce the amount of IPs used and clean somethings up. Each private IP would get translated into a public IP so that everything works fine and each computer would have access to the internet.

The RFC-1918 standard created private IP addresses to prevent a shortage of public IP addresses available to ISPs and consumers. Private IP addresses are commonly found in schools, homes, businesses or anywhere that contains a network.

## Ranges

These are the ranges for IPs that ISPs give out to companies/organizations that have a certain number of devices.

### Public IPv4 Ranges

Here are some default subnet masks for the various classes of IPv4 addresses:

![[Pasted image 20230329225825.png]]

IP addresses are assigned to organizations and blocks, there are 5 classes of IP addresses but for the A+ exam you'll only need to know three (A, B and C).

|Class|First Octet Address|Default Subnet Mask|Number of Hosts|Number of Networks|Notes|
|-|-|-|-|-|-|
|A|1-126|255.0.0.0|16 million|126|Typically given to large organizations|
|B|128-191|255.255.0.0|65 thousand|16 thousand|Typically given to medium sized organizations|
|C|192-223|255.255.255.0|254|2 million|Typically given to small organizations or small home networks|

### Private IPv4 Ranges

These are the ranges for private IP addresses:

|Class|Range|Subnet Mask|
|-|-|-|
|A|10.0.0.0-10.255.255.255|255.0.0.0|
|B|172.16.0.0-172.31.255.255|255.255.0.0|
|C|192.168.0.0-192.168.255.255|255.255.255.0|
