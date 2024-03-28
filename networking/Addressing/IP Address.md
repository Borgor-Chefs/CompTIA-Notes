---
tags:
  - networking
---
# Internet Protocol Address

This is a numeric identifier for computers that want to connect to a network, this is required for a device to communicate on a network.

- IP address versions
    - [[#IPv4]]
    - [[#IPv6]]
- [[#Reserved IP Addresses]]
- types of IP addresses
    - [[Subnets|Subnet (Mask)]]
    - [[#Public IP Address]]
    - [[#Private IP Address]]
    - [[#Gateway IP Address]]
    - [[#Virtual IP Address (VIP)]]
- IP address ranges (class)
    - [[#Public IPv4 Ranges]]
    - [[#Private IPv4 Ranges]]

## Versions

### IPv4

This is a 32-bit numeric address written as four numbers separated by periods. Each segment is called an octet, ranging from 0 to 255 e.g., 127.0.0.1.

There are $2^{32}$ or 4,294,967,296 possible addresses.

>The first octet 127 is reserved for loopback testing.

An IPv4 address consists of two parts: a network address and a host address.

### IPv6

The original architects of networking thought that IPv4 would suffice and that we wouldn't run out of possible IP addresses.

They were wrong, so they invented IPv6 which is a 128-bit hexadecimal address, e.g., 76dc:4f59:34cf:71cd:9dc6:89cd:45d6:67a2. Each 4-byte segment is separated by a colon.

There are $2^{128}$ or 340,282,366,920,938,463,463,374,607,431,768,211,456 possible addresses.

## Types

There are different types of [[#IPv4|IPv4]] addresses, they are:

- [[Subnets]]
- [[#Public IP Address]]
- [[#Private IP Address]]
- [[#Gateway IP Address]]
- [[#Virtual IP Address (VIP)]]

IPv4 addresses have different classifications and ranges for both public and private addresses. See [[#Ranges|here]].

### Public IP Address

This is the IP address that's outward facing to both the internet and your ISP. This is typically assigned to your [[Router]].

### Private IP Address

This is your internal IP used for networking in your [[Network Types#Local Area Network (LAN)|LAN]] network. Only your device and the other devices on your network will use this to communicate with you.

If a device outside of your network wants to communicate with you, say a gaming server in the USA and you're in Canada, they will use your public IP to communicate with you, and you with them.

Finally, in order for your computer on your local network to actually receive the messages, your [[Router]] or [[Switch]] will [[NAT]] to translate the public IP to your computer's private IP.

>This kind of IP is something that cannot directly access the internet nor is it publicly registered, and this is for good reason. Imagine having a business with 10 computers, you might want 10 public IPs. This isn't a good idea because this could lead to a shortage of addresses.
>
>Instead, if you have one public IP and 10 private IPs, this would reduce the amount of IPs used and clean somethings up. Each private IP would get translated into a public IP so that everything works fine and each computer would have access to the internet.
>
>The RFC-1918 standard created private IP addresses to prevent a shortage of public IP addresses available to ISPs and consumers. Private IP addresses are commonly found in schools, homes, businesses or anywhere that contains a network.

### Gateway IP Address

This is the IP address of your [[Router]] and it must be on the same [[#Subnet (Mask)|subnet]] as your computer. This is what allows you to communicate outside of your local subnet.

>This is generally either the first possible IP address on your subnet or the last possible IP address.
>E.g., 10.0.0.1 or 10.255.255.254

### Virtual IP Address (VIP)

This isn't associated with a [[Network Interface Card|physical network adaptor]] but rather a virtual machine or an internal [[Router]] address.

## Ranges

These are the ranges for IPs that ISPs give out to companies/organizations that have a certain number of devices.

>Apparently in modern networking, IP classes aren't really adhered to. Each company/network will probably have it's own setup.

| Class | Public IP Range              | Private IP Range               | Subnet Mask   | Number of Networks | Number of hosts per Network |
| ----- | ---------------------------- | ------------------------------ | ------------- | ------------------ | --------------------------- |
| A     | 1.0.0.1 to 127.255.255.254   | 10.0.0.0 to 10.255.255.255     | 255.0.0.0     | 126                | 16,777,214                  |
| B     | 128.0.0.1 to 191.255.255.254 | 172.16.0.0 to 172.31.255.255   | 255.255.0.0   | 16,382             | 65,534                      |
| C     | 192.0.0.1 to 223.255.255.254 | 192.168.0.0 to 192.168.255.255 | 255.255.255.0 | 2,097,150          | 254                         |
| D     | 224.0.0.1 to 239.255.255.254 | undefined                      | undefined     | undefined          | undefined                   |
| E     | 240.0.0.1 to 255.255.255.254 | undefined                      | undefined     | undefined          | undefined                   |

>Class D IP addresses are reserved for [[Network Broadcasting Methods#Multicast|multicast networking]].
>Class E IP addresses are reserved.

| Name               | IP Address                     | Usages                                                                        |
| ------------------ | ------------------------------ | ----------------------------------------------------------------------------- |
| Loopback Address   | 127.0.0.1 to 127.255.255.254   | Basically just for testing the networking connectivity on your local machine. |
| Reserved Addresses | 240.0.0.1 to 254.255.255.254   | Reserved for "Class E" addresses.                                             |
| APIPA              | 169.254.0.1 to 169.254.255.254 | Reserved by IETF for APIPA addresses.                                         |

>For full list of reserved IP addresses, see [here](https://en.wikipedia.org/wiki/Reserved_IP_addresses).
