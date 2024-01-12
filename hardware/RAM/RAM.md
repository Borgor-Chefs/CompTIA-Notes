Tags: [#ram]

# Random Access Memory (RAM)

RAM is volatile storage which requires constant power to store data. RAM is quick, faster storage for the [[CPU]] to access.

RAM is stored on the [[The Motherboard|motherboard]] in modules called [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMMs]]. These DIMMs come in different memory sizes from 128 MB to 64 GB.

RAM also has speeds and versions, the faster the RAM the better because that means that more data travels from RAM to the [[CPU]].

[[The Motherboard|Motherboards]] have [[RAM Slots|RAM slots]] tailored to a specific version of RAM, meaning that you cannot interchange [[#DDR/DDR1 (Double Data Rate)|DDR]], [[#DDR2|DDR2]], [[#DDR3|DDR3]] and other RAM sticks.

## Types of RAM

- [[#DRAM (Dynamic RAM)]]
- [[#SRAM (Static RAM)]]
	- [[#DDR/DDR1 (Double Data Rate)|DDR1 (Double Data Rate)]]
	- [[#DDR2]]
	- [[#DDR3]]
	- [[#DDR3]]
	- DDR4
	- DDR5
- [[#Rambus Dynamic RAM (RDRAM)]]
- [[#Error Correcting Code (ECC)|ECC RAM]]

### DRAM (Dynamic RAM)

This type of RAM uses capacitors and has to be refreshed often.

### SRAM (Static RAM)

This type of RAM uses transistors and does **not** have to be refreshed, making this faster than [[#DRAM (Dynamic RAM)|DRAM]]. But SRAM is also very expensive, SRAM is comparable to the memory caches used by the [[CPU]].

### Synchronous Dynamic RAM (SDRAM)

This type of technology is used today in RAM [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMMs]]. The difference between [[#DRAM (Dynamic RAM)|DRAM]] and SDRAM is that SDRAM operates sychronously with the system clock where as DRAM does not.

SDRAM is therefore faster than [[#DRAM (Dynamic RAM)|DRAM]] because the signals are in synch with the [[CPU]]. In other words, the CPU does not have to wait for the DRAM to respond.

![[Pasted image 20220821224246.png]]

SDRAM operates at different speeds depending on the hardware. It will have a label of PC-XXX in our case let's say it's PC-100. The 100 in PC-100 stands for MHz or the speed at which that SDRAM module operates.

SDRAM only comes in 64-bit modules and remember that because of [[RAM Slots|this]], it has a 8 byte wide bus.

To calculate the bandwidth (speed of data transfer, e.g., MB/s) of the RAM, we multiply the speed and the bus together to obtain the bandwidth;
$$
100\text{ MHz }\times8\text{ bytes } = 800\text{ MB/s}
$$

#### DDR/DDR1 (Double Data Rate)

![[Pasted image 20220821224522.png]]

This type of [[#Synchronous Dynamic RAM (SDRAM)|SDRAM]] technology uses both the rising and falling edges of the system clock to send data, making this type of RAM technology twice as fast than any other.

DDR also has 184 pins.

![[Pasted image 20220821224720.png]]

Unlike regular [[#Synchronous Dynamic RAM (SDRAM)|SDRAM]], [[#DDR/DDR1 (Double Data Rate)|DDR]] RAM uses the total bandwidth in its label name.

For the picture above, the 2700 in PC-2700 is the bandwidth. We can calculate the speed of the RAM module by some simple math; (some rounding involved)
$$
2700\text{ MB/s }\div8\text{ bytes } = 333\text{ MHz}
$$

#### DDR2

![[Pasted image 20220822200358.png]]

This is the successor to [[#DDR/DDR1 (Double Data Rate)|DDR]] for it is faster, allows for higher bus speeds and it uses less power than DDR. DDR2 also uses 240 pins.

#### DDR3

DDR3 is twice as fast as [[#DDR2|DDR2]] RAM with a bandwidth of over 12800 MB/s. Like DDR2, it also has 240 pins. The main difference between this and DDR2 is that the notches are in different places.

### Rambus Dynamic RAM (RDRAM)

This type of RAM ([[RAM Slots#Rambus Inline Memory Module (RIMM)|RIMM]]) debuted in 1999 and was developed by Rambus Inc. It has 184 pins and looks similar to DIMMs. At the time this was a breakthrough in the speeds of memory but has fallen behind due to the advancement of technology in [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMMs]].

RIMMs debuted with a speed of 800 MHz but it only had a 2 byte wide bus, the total bandwidth being 1600 MB/s.

RIMM technology was designed to work with a continuous signal and all memory slots on the motherboard must be used in order for this type of RAM to work properly. If there are no RIMMs available, Continuity RIMMs (C-RIMM) which are essentially dummy RIMMs which don't do anything, can be used to fill the slots of the motherboard.

## Error Correcting Code (ECC)

This detects if the data was correctly processed by the memory module and will make a correction if needed.

![[Pasted image 20220824220246.png]]

You can identify ECC RAM v.s. non-ECC RAM via. the amount on memory chips on the RAM stick. On a standard [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMM]] RAM module, non-ECC RAM will have 8 memory chips whereas ECC RAM will have 9 memory chips. See picture above.

>ECC RAM is generally considered slower than regular non-ECC RAM.

Most RAM modules today are non-ECC thanks to the advancement in technology which makes non-ECC RAM more stable. ECC RAM is mostly used in servers which are up and running all the time and that need to ensure that data is read from/written to correctly as a precaution.

## Buffered v.s. Unbuffered RAM

Buffered RAM (registered RAM) is made to add stability to RAM. It adds an extra register between the RAM and the memory controller where data gets stored (buffered) before it gets sent to the CPU.

This adds stability, reliability and lessens the electical load of computer systems which have a lot of memory modules installed, particularily servers.
