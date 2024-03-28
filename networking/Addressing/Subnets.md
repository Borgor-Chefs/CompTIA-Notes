---
tags:
  - networking
---
# Subnets

A subnet is an [[IP Address#IPv4|IPv4 address]] which dictates what part of the full IPv4 address is for the network and for the host. This is a way to break apart a bigger network into smaller chunks to improve performance.

![[Pasted image 20230329225554.png]]

Above is how an [[#IPv4|IPv4 address]] is broken down into its two parts: network and host. We use a mask (the network portion of the mask will always be 255) to deduce what part of the IP is for the network and for the host.

The network portion will target devices on a certain network and the host portion will target the actual device.

>With subnets, you **cannot** have an IP that is the host network address nor the broadcast network address. Things will just not work.

## Notation

There are a couple of ways to represent subnet masks.

### IPv4 Subnet Notation

Take the subnet mask 255.255.240.0, it can be represented in a couple of ways:

>That mask in bits is: 11111111.11111111.11110000.00000000

- 255.255.240.0 - proper subnet notation
- 172.68.11.4/20 - slash, prefix or CIDR notation
    - the "/20" comes from the number of 1s in the subnet mask

### IPv6 Subnet Notation

something

## Subnet Mask Creation

Historically, your computer would determine its subnet mask, broadcast address and such from the class of IP your computer was assigned. This turned out to be a bad idea for reasons and now, instead of having subnets determined by a class, subnets are now arbitrarily determined by their network administrators.

This is called Variable Length Subnet Masks (VLSM). The point of this is to allow for flexibility when creating networks.

### Classful v.s. Classless Subnets

With VLSM created to give flexibility to networks, there's a difference between classful and classless subnets:

- classful: your subnet mask is determined by the class of IP address your computer is using
- classless: your subnet mask is manually determined by the network administrator

## Calculations with Subnets

>This is a good video on how to quickly calculate subnet IDs, [link](https://www.youtube.com/watch?v=XMzLpGKTu50).
>This one too, [link](https://www.youtube.com/watch?v=SWy0MRfkXpQ).

From a subnet mask and your IP address, you can calculate the network address and the broadcast address of your network.

![[Pasted image 20240327172838.png]]

See this python sample code in order to calculate every address shown above:

```py
def get_network_address(addr, mask):
    return addr & mask

def get_first_host(addr, mask):
    return get_network_address(addr, mask) + 1

def get_broadcast_address(addr, mask):
    return (addr & mask) | (!mask)

def get_last_host(addr, mask):
    return get_broadcast_address(addr, mask) - 1
```

### Number of Hosts per Subnet

The formulae are as follows:

$$
\begin{gather}
\text{number of subnets}=2^{\text{subnet bits}}\\
\text{hosts per subnet}=2^{\text{host bits}}-2\\
\end{gather}
$$

For example, if your IP address is 10.1.1.0/24, using the formulae we obtain:

$$
\begin{gather}
\text{number of subnets}=2^{24-8}=2^{16}=65,536\\
\text{hosts per subnet}=2^8-2=256-2=254\\
\end{gather}
$$

>The reason why we subtract 8 from the subnet bits is because those 8 bits are from the network subnet mask, they're redundant and will give the wrong answer.
>
>The reason why we subtract two from the hosts is because one address is for the network and the other is for the broadcast address.

## Defining Subnets

![[Pasted image 20240327201729.png]]

Network administrators, when creating a network, have a large pool of IP addresses. While it's to have a network with 16 million possible hosts, but only like 20 devices, once your network gets 1,000, 10,000 or more devices, your network's performance will come to an absolute fucking screeching halt.

The above image shows that from your classful subnet mask, you can extend your subnet mask further to create a smaller network.

The reason why subnetting improves network performance is because it isolates and compartmentalizes traffic into smaller chunks. This way, instead of a computer receiving a million broadcasts, it will only receive the broadcasts on its network. 

>This is what ISPs do in order to create as many public IPs as possible. They subnet the ever living shit out of the address space they have.

## IPv4 Subnets Reference

![[IP Address#Ranges]]
