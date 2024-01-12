---
tags:
  - ram
---
# Random Access Memory (RAM)

RAM is volatile storage which requires constant power to store data. RAM is quick, faster storage for the [[CPU]] to access.

With RAM, there are:

- [[RAM Types|types]] - the types/iterations of RAM
- [[RAM Modes|modes]] - the modes the motherboard can communicate with the RAM sticks
- [[RAM Slots|slots]] - the physical place you insert the RAM stick into the motherboard

## Single Sided vs. Double Sided RAM

This doesn't necessarily refer to the physical location of memory chips that are on the sides of the memory module.

![[Pasted image 20220824215931.png]]

This actually refers to the groups of memory chips that the memory controller can access. For example, double sided RAM means that there are two groups of memory chips on a RAM stick. It does not matter if the memory chips are on the same side or opposite sides.

The memory controller can only access these groups of memory chips one at a time. Since single sided RAM allows the memory controller to access all the memory chips at the same time, this makes single sided RAM faster than double sided RAM.

## How Do Programs Get Loaded?

When a computer wants to run a program the program is first loaded into RAM and after it is loaded into RAM, the [[CPU]] will now read and execute the program.

Sometimes when the program is too big or if there isn't enough RAM to spare, part of the program will stay unloaded on the [[HDD|hard drive]] and when needed, it will be loaded into RAM then processed by the CPU.

To fix this issue, simply increase the amount of RAM of the computer.
