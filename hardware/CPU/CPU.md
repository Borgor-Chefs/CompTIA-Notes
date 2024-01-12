Tags: [#cpu]

# The Central Processing Unit (CPU)

![[Pasted image 20220826153959.png]]

This is the module which performs computational tasks such as addition, subtraction, multiplication, moving data from register to register, controlling [[RAM|memory]] and other important tasks.

The CPU is the largest component on the [[The Motherboard|motherboard]], typically after the CPU is inserted into a [[#^062ecf|socket]] it is covered by a [[Heat Sink|heat sink]] and a [[Fans|fan]] or has a [[Water Cooling|water cooling]] component.

## CPU Bit Sizes

CPUs come in 32-bit (old) and 64-bit (standard) versions, the main difference being how the CPU handles memory.

- 32-bit can address $2^{32}$ bytes of information, equivalent to 4 gigabytes (GB).
- 64-bit can address $2^{64}$ bytes of information, equivalent to 16 exabytes (EB).
	- This is about 4 billion times more than a 32-bit processor.
	- This number is so huge that it is virtually infinite since (in 2022) we will never need to use that much [[RAM|memory]].

## Manufacturers

These are the companies which produce CPUs amongst other hardware but there are two major companies;

- [[#^289a44|Intel]]
- [[#^7991e9|Advanced Micro Devices]] (AMD)

### Intel

^289a44

Intel was the largest manufacturer of processors and was founded in the late 1960s. Some examples of their CPUs are:

- 286
- 386
- 486
- Celeron
- Pentium
- i3
- i5
- i7
- i9

### Advanced Micro Devices (AMD)

^7991e9

AMD is the largest manufacturer of processors and was founded in the late 1960s like [[#^289a44|Intel]]. Some of their CPUs are:

- k5
- k6
- Athlon
- Duron
- Sempron
- Ryzen
- Threadripper

## Sockets

^062ecf

CPUs get inserted into [[CPU Sockets|sockets]], they essentially act as the bridge between the [[The Motherboard|motherboard]] and the CPU.

## Speeds

The speed of a CPU is measured in MHz or GHz, for example; a CPU at a speed of...

- 1 MHz has 1 million cycles per second
- 500 MHz has 500 million cycles per second
- 1 GHz has 1 billion cycles per second
- 3 GHz has 3 billion cycles per second

## Cores

![[Pasted image 20220826154212.png]]

This is where the reading and execution of instructions takes place, CPUs can have multiple cores. A single core processes one instruction at a time. The more cores, the more processing power since there are more instructions being executed per cycle.

CPUs which have multiple cores are called "multi-core" processors, for example...

- A dual core CPU has 2 cores
- A quad core CPU has 4 cores

## Memory Cache

![[Pasted image 20220826160131.png]]

This is the CPU's internal memory. Caches are up of very fast [[RAM#^e7da69|SRAM]].

The cache's purpose is to hold data and instructions waiting to be used by the processor, it will prioritize data and instructions that are very frequently used by the CPU to improve the overall speed of the CPU.

### Cache Levels

The CPU will consult its caches in order of their speeds, prioritizing the fastest first then the slowest. If the CPU cannot find what it is looking for in any of its caches, it will look for it in memory.

#### Level 1 Cache, L1 or Primary Cache

^66b314

This type of cache is located on the processor itself and is the fastest form of cache.

#### Level 2 Cache, L2 or External Cache

This type of cache is located either on the [[The Motherboard|motherboard]] or on the CPU itself (newer CPUs). This is used to catch recent data accesses from the processor that were not caught by the [[#^66b314|level 1 cache]].

Level 2 cache is not as fast as [[#^66b314|level 1 cache]], but it is a lot bigger.