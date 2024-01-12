Tags: [#ram]

# Random Access Memory (RAM)

RAM is volatile #storage which requires constant power to store data. RAM is quick, faster storage for the [[CPU]] to access.

RAM is stored on the [[The Motherboard|motherboard]] in modules called [[RAM Slots#^7a04f0|DIMMs]]. These DIMMs come in different memory sizes from 128 MB to 64 GB.

RAM also has speeds and versions, the faster the RAM the better because that means that more data travels from RAM to the [[CPU]].

## Types of RAM

### Dynamic RAM

^ea2a9c

This type of RAM uses capacitors and has to be refreshed often.

### Static RAM

This type of RAM uses transistors and does **not** have to be refreshed, making this faster than [[#^ea2a9c|DRAM]]. But SRAM is also very expensive, SRAM is comparable to the memory caches used by the [[CPU]].

### Synchronous Dynamic RAM (SDRAM)

This type of technology is used today in RAM [[RAM Slots#^7a04f0|DIMMs]]. The difference between [[#^ea2a9c|DRAM]] and SDRAM is that SDRAM operates sychronously with the system clock where as DRAM does not.

SDRAM is therefore faster than [[#^ea2a9c|DRAM]] because the signals are in synch with the [[CPU]]. In other words, the CPU does not have to wait for the DRAM to respond.

#### SDRAM Speeds

![[Pasted image 20220821224246.png]]

SDRAM operates at different speeds depending on the hardware. It will have a label of PC-XXX in our case let's say it's PC-100. The 100 in PC-100 stands for MHz or the speed at which that SDRAM module operates.

SDRAM only comes in 64-bit modules and remember that because of [[RAM Slots|this]], it has a 8 byte wide bus.

To calculate the bandwidth (speed of data transfer, e.g., MB/s) of the RAM, we multiply the speed and the bus together to obtain the bandwidth;
$$
100\text{ MHz }\times8\text{ bytes } = 800\text{ MB/s}
$$

### Double Data Rate (DDR)

^3f049c

![[Pasted image 20220821224522.png]]

This type of RAM technology uses both the rising and falling edges of the system clock to send data, making this type of RAM technology twice as fast than any other.

DDR also has 184 pins.

#### DDR1 Speeds

![[Pasted image 20220821224720.png]]

Unlike SDRAM, [[#^3f049c|DDR]] RAM uses the total bandwidth in its label name.

For the picture above, the 2700 in PC-2700 is the bandwidth. We can calculate the speed of the RAM module by some simple math; (some rounding involved)
$$
2700\text{ MB/s }\div8\text{ bytes } = 333\text{ MHz}
$$

### DDR2

This is the successor to [[#^3f049c|DDR]] for it is faster, allows for higher bus speeds and it uses less power than DDR. DDR2 also uses 240 pins.

## How Do Programs Get Loaded?

When a computer wants to run a program the program is first loaded into RAM and after it is loaded into RAM, the [[CPU]] will now read and execute the program.

Sometimes when the program is too big or if there isn't enough RAM to spare, part of the program will stay unloaded on the [[HDD|hard drive]] and when needed, it will be loaded into RAM then processed by the CPU.

To fix this issue, simply increase the amount of RAM of the computer.