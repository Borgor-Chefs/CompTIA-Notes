Tags: [#ram]

# Random Access Memory (RAM)

RAM is volatile #storage which requires constant power to store data. RAM is quick, faster storage for the [[CPU]] to access.

RAM is stored on the [[The Motherboard|motherboard]] in modules called [[RAM Slots#^7a04f0|DIMMs]]. These DIMMs come in different memory sizes from 128 MB to 64 GB.

RAM also has speeds and versions, the faster the RAM the better because that means that more data travels from RAM to the [[CPU]].

[[The Motherboard|Motherboards]] have [[RAM Slots|RAM slots]] tailored to a specific version of RAM, meaning that you cannot interchange [[#^3f049c|DDR]], [[#^78fa7d|DDR2]], [[#^0a74fc|DDR3]] and other RAM sticks.

## How Do Programs Get Loaded?

When a computer wants to run a program the program is first loaded into RAM and after it is loaded into RAM, the [[CPU]] will now read and execute the program.

Sometimes when the program is too big or if there isn't enough RAM to spare, part of the program will stay unloaded on the [[HDD|hard drive]] and when needed, it will be loaded into RAM then processed by the CPU.

To fix this issue, simply increase the amount of RAM of the computer.

## Types of RAM

^fca6da

### Dynamic RAM

^ea2a9c

This type of RAM uses capacitors and has to be refreshed often.

### Static RAM

This type of RAM uses transistors and does **not** have to be refreshed, making this faster than [[#^ea2a9c|DRAM]]. But SRAM is also very expensive, SRAM is comparable to the memory caches used by the [[CPU]].

### Synchronous Dynamic RAM (SDRAM)

^94365d

This type of technology is used today in RAM [[RAM Slots#^7a04f0|DIMMs]]. The difference between [[#^ea2a9c|DRAM]] and SDRAM is that SDRAM operates sychronously with the system clock where as DRAM does not.

SDRAM is therefore faster than [[#^ea2a9c|DRAM]] because the signals are in synch with the [[CPU]]. In other words, the CPU does not have to wait for the DRAM to respond.

![[Pasted image 20220821224246.png]]

SDRAM operates at different speeds depending on the hardware. It will have a label of PC-XXX in our case let's say it's PC-100. The 100 in PC-100 stands for MHz or the speed at which that SDRAM module operates.

SDRAM only comes in 64-bit modules and remember that because of [[RAM Slots|this]], it has a 8 byte wide bus.

To calculate the bandwidth (speed of data transfer, e.g., MB/s) of the RAM, we multiply the speed and the bus together to obtain the bandwidth;
$$
100\text{ MHz }\times8\text{ bytes } = 800\text{ MB/s}
$$

#### Double Data Rate (DDR/DDR1)

^3f049c

![[Pasted image 20220821224522.png]]

This type of [[#^94365d|SDRAM]] technology uses both the rising and falling edges of the system clock to send data, making this type of RAM technology twice as fast than any other.

DDR also has 184 pins.

![[Pasted image 20220821224720.png]]

Unlike regular [[#^94365d|SDRAM]], [[#^3f049c|DDR]] RAM uses the total bandwidth in its label name.

For the picture above, the 2700 in PC-2700 is the bandwidth. We can calculate the speed of the RAM module by some simple math; (some rounding involved)
$$
2700\text{ MB/s }\div8\text{ bytes } = 333\text{ MHz}
$$

#### DDR2

^78fa7d

![[Pasted image 20220822200358.png]]

This is the successor to [[#^3f049c|DDR]] for it is faster, allows for higher bus speeds and it uses less power than DDR. DDR2 also uses 240 pins.

#### DDR3

^0a74fc

DDR3 is twice as fast as [[#^78fa7d|DDR2]] RAM with a bandwidth of over 12800 MB/s. Like DDR2, it also has 240 pins. The main difference between this and DDR2 is that the notches are in different places.

### Rambus Dynamic RAM (RDRAM)

This type of RAM ([[RAM Slots#^201aea|RIMM]]) debuted in 1999 and was developed by Rambus Inc. It has 184 pins and looks similar to DIMMs. At the time this was a breakthrough in the speeds of memory but has fallen behind due to the advancement of technology in [[RAM Slots#^7a04f0|DIMMs]].

RIMMs debuted with a speed of 800 MHz but it only had a 2 byte wide bus, the total bandwidth being 1600 MB/s.

RIMM technology was designed to work with a continuous signal and all memory slots on the motherboard must be used in order for this type of RAM to work properly. If there are no RIMMs available, Continuity RIMMs (C-RIMM) which are essentially dummy RIMMs which don't do anything, can be used to fill the slots of the motherboard.

## Types of RAM Modes

^e848c3

There are "modes" to how the [[The Motherboard|motherboard]] can communicate with RAM sticks. They are...

- Single Channel
- [[#^423b74|Dual Channel]]
- [[#^c39b2c|Triple Channel]]

Each mode indicates the amount of RAM sticks that can be communicated with simultaneously. This improves the speed at which memory is read/wrote to since this happens per clock cycle.

If you are running...

- single channel mode, it can transfer 64-bits of information per clock cycle
- [[#^423b74|dual channel]] mode, 128-bits/clock cycle
- [[#^c39b2c|triple channel]] mode, 192-bits/clock cycle

### Dual Channel Mode

^423b74

To meet the demands of faster processors and memory controllers, the dual channel mode was developed so that the memory controller could interface with two [[RAM Slots#^7a04f0|DIMMs]] simultaneously. However these DIMMs must be identical.

In order for dual channel mode to function, the [[The Motherboard|motherboard]] must be equipped to work in dual channel mode, the [[RAM Slots#^7a04f0|DIMMs]] must be identical to each other in speed, size and features. The DIMMs must be inserted into the motherboard in a specific slot configuration.

![[Pasted image 20220824214533.png]]

[[The Motherboard|Motherboards]] will typically have color codings (see above image) to indicate to the user what order/places to place the [[RAM Slots#^7a04f0|DIMMs]].

### Triple Channel Mode

^c39b2c

An uncommon method of communication with RAM is triple channel mode, where as the name suggests the memory controller has the ability to interface with 3 [[RAM Slots#^7a04f0|DIMMs]] simultaneously.

## Single Sided v.s. Double Sided RAM

This doesn't necessarily refer to the physical location of memory chips that are on the sides of the memory module.

![[Pasted image 20220824215931.png]]

This actually refers to the groups of memory chips that the memory controller can access. For example, double sided RAM means that there are two groups of memory chips on a RAM stick. It does not matter if the memory chips are on the same side or opposite sides.

The memory controller can only access these groups of memory chips one at a time. Since single sided RAM allows the memory controller to access all the memory chips at the same time, this makes single sided RAM faster than double sided RAM.

## Error Correcting Code (ECC)

This detects if the data was correctly processed by the memory module and will make a correction if needed.

![[Pasted image 20220824220246.png]]

You can identify ECC RAM v.s. non-ECC RAM via. the amount on memory chips on the RAM stick. On a standard [[RAM Slots#^7a04f0|DIMM]] RAM module, non-ECC RAM will have 8 memory chips whereas ECC RAM will have 9 memory chips. See picture above.

Most RAM modules today are non-ECC thanks to the advancement in technology which makes non-ECC RAM more stable. ECC RAM is mostly used in servers which are up and running all the time and that need to ensure that data is read from/written to correctly as a precaution.

## Buffered v.s. Unbuffered RAM

Buffered RAM (registered RAM) is made to add stability to RAM. It adds an extra register between the RAM and the memory controller where data gets stored (buffered) before it gets sent to the CPU.

This adds stability, reliability and lessens the electical load of computer systems which have a lot of memory modules installed, particularily servers.