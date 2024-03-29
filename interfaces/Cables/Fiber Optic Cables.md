---
tags:
  - networking
  - cable
---
# Fiber Optic Cable

These cables use light, specifically the visible light spectrum to transmit data over a physical medium. The signal is also slow to degrade which makes it perfect for transmission over long distances.

There's no RF signal, making it harder (not impossible) to monitor or tap. And because there's no RF signal, it's immune to RF interference.

## Anatomy

![[Pasted image 20240317170545.png]]

The cable itself is made up of three parts;

- the core
- the cladding
- the buffer coating

![[Pasted image 20240317170704.png]]

>The above is an example of a [[#Standard/Subscriber Connector (SC)|SC]] cable.

The "ferrule" surrounds the fiber core to protect it from damage and interference.

Other topics:

- [[#Problems with Fiber Optic Cables]]
- 

## Cables

- connector ending types
    - [[#Ultra-polished Connectors (UPC)]]
    - [[#Angled-polished Connectors (APC)]]
- connector types
    - [[#Straight Tip (ST)]]
    - [[#Local/Lucent Connector (LC)]]
    - [[#Standard/Subscriber Connector (SC)]]
    - [[#Mechanical Transfer Registered Jack (MT-RJ)]]
- cable types
    - [[#Single Mode Fiber (SMF)]]
    - [[#Multimode Fiber (MMF)]]

### Connector Ending Types

As described in the [[#Problems with Fiber Optic Cables]] section, some light gets reflected back to the source, therefore there are two solutions to this: UPC and APC

#### Ultra-polished Connectors (UPC)

![[Pasted image 20240319162503.png]]

This is where the ferrule end-face radius polished at a zero degree angle, but this produces a high return loss.

#### Angled-polished Connectors (APC)

![[Pasted image 20240319162512.png]]

This is where the ferrule end-face radius polished at a eight degree angle, this produces a lower return loss, but generally higher insertion loss than [[#Ultra-polished Connectors (UPC)]].

### Connector Types

#### Straight Tip (ST)

![[Pasted image 20220828205530.png]]

This is a fiber optic cable connector and uses a half-twist bayonet type of lock. Commonly used with [[#Single-mode Fiber (SMF)|single-mode fiber optic cable]].

#### Local/Lucent Connector (LC)

![[Pasted image 20220828205636.png]]

This is another fiber optic cable like the [[#Straight Tip (ST)|ST connector]] and is similar to the [[Digital Cables#Register Jack 45 (RJ-45) (Ethernet Cable)|RJ-45]] style of connector. This is commonly used between floors on a building.

#### Standard/Subscriber Connector (SC)

![[Pasted image 20220828205838.png]]

This is a fiber optic cable that uses a push-pull connector similar to [[Coaxial Cables#RCA|audio and video plugs]]. Like the [[#Local/Lucent Connector (LC)|LC connector]] it is also used between the floors of a building.

## Mechanical Transfer Registered Jack (MT-RJ)

![[Pasted image 20240319161458.png]]

This is a really small type of fiber optic connector. For example, if a networking hardware company wanted to put the maximum amount of connectors into the smallest possible space, they would use this type of connector.

### Cable Types

Between these two cable types, the [[#Single-mode Fiber (SMF)|single mode fiber]] has a much denser cladding than the [[#Multi-mode Fiber (MMF)|multi-mode fiber]].

#### Single-mode Fiber (SMF)

![[Pasted image 20240317170931.png]]

This type of cable only allows light to enter it at a certain angle and at certain wavelength. This uses an expensive light source such as a laser.

This is used for long-range communication up to 100km.

#### Multi-mode Fiber (MMF)

![[Pasted image 20240317170846.png]]

This type of cable allows light to reflect off the walls of the cable and usually uses an inexpensive light source like an LED. It is called "multi-mode" fiber because it allows for various wavelengths of light to be passed through.

This is used for short-range communication up to 2km.

## Problems with Fiber Optic Cables

When dealing with light, we must consider and deal with the laws of physics (naturally just like with [[Digital Cables|copper cables]], but now were dealing with different parts of physics).

One of the problems with fiber optics is the "return loss" i.e., how much light is reflected back to the source. This creates an inefficiency.

## Wavelength-Division Multiplexing

![[Pasted image 20240320163929.png]]

This is bidirectional communication over a single strand of fiber. Each wavelength uses its own color. This is basically what broadband is to fiber optics.

There is also:

- Coarse Wavelength-Division Multiplexing
    - this uses four different wave lengths and uses the [[Ethernet Standard|10GBASE-LX4]] standard and has a maximum throughput of 3.125 Gbit/s
- Dense Wavelength-Division Multiplexing
    - this uses a fuck ton of different wave lengths, or "carriers" to transmit data
    - this has 160 signals and increases the throughput to 1.6 Tbit/s
