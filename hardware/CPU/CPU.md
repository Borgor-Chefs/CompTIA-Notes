Tags: [#cpu]

# The Central Processing Unit (CPU)

This is the module which performs computational tasks such as addition, subtraction, multiplication, moving data from register to register, controlling [[RAM|memory]] and other important tasks.

## The CPU Socket

^595892

The processor socket is the place on the [[The Motherboard|motherboard]] where the CPU is placed. It is a square plastic or metal holder with multiple holes which are meant for the pins of the CPU. This allows for the physical & electrical contact between the motherboard and the CPU.

A modern CPU socket is called a zero insertion force or ZIF. Where the CPU is installed with no force (typically you just place it in in the correct manner).

### Socket Design Packages

There are multiple CPU [[#^595892|socket]] designs which are called "packages".

#### Pin Grid Array (PGA)

A PGA is a typical square ZIF [[#^595892|socket]] design with holes and a lock down lever.

#### Land Grid Array (LGA)

The modern design for [[#^595892|socket]] design packages. This is a socket with a cover and a lever which covers the CPU with the cover. The socket itself has pins where the CPU does not instead, the CPU has pads which rest on the pins, making contact with the socket.

### Socket Types

There are two main [[#^595892|socket]] types which are categorized by two different brands:

- [[#^d215df|Intel]]
- [[#^0556b8|AMD]]

#### Intel

^d215df

These are the socket types designed by Intel. They are sorted by the increasing amount of pins present within the socket.

##### LGA 775 a.k.a. Socket T

^66c202

![[Pasted image 20220824223229.png]]

Released in 2004, this socket type has 775 pins and was meant to succeed socket 478. This socket type was designed for Pentium 4 and Pentium dual core processors.

##### LGA 1150 a.k.a. Socket H3

![[Pasted image 20220824224025.png]]

Released in 2013, this socket type has 1150 pins and is the successor to the [[#^ce731c|LGA 1155]]. This socket supports Haswell and Broadwell based microprocessors.

##### LGA 1155 a.k.a. Socket H2

^ce731c

![[Pasted image 20220824223833.png]]

Released in 2011, this socket type has 1155 pins and was meant to replace the [[#^d56d9d|LGA 1156]]. This socket type was designed for Intel CPUs that use the Sandy Bridge and Ivy Bridge architecture.

Note that the CPUs that are made for the LGA 1155 socket and [[#^d56d9d|LGA 1156]] socket are not compatible with each other due to their physical differences.

##### LGA 1156 a.k.a. Socket H/H1

^d56d9d

![[Pasted image 20220824223521.png]]

Released in 2009, this socket type has 1156 pins. This socket type was designed for the Intel Core i3 and i5 processors.

##### LGA 1366 a.k.a. Socket B

^3164e1

![[Pasted image 20220824223355.png]]

Released in 2008, this socket type has 1366 pins and was meant to succeed socket [[#^66c202|LGA 775]]. This socket type was designed for the Intel Core i7 and Xeon processors.

##### LGA 2011 a.k.a. Socket R

![[Pasted image 20220824224327.png]]

Released in 2011, this socket type has 2011 pins and has succeeded the [[#^3164e1|LGA 1366]]. This socket was designed for high-performance CPUs that are based on the Sandy Bridge and Ivy Bridge processors.

#### AMD

^0556b8