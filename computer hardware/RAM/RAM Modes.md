---
tags:
  - ram
---
# Types of RAM Modes

There are "modes" to how the [[The Motherboard|motherboard]] can communicate with [[RAM Types|RAM Types]] sticks. They are...

- Single Channel
- [[#Dual Channel Mode|Dual Channel]]
- [[#Triple Channel Mode|Triple Channel]]

Each mode indicates the amount of RAM sticks that can be communicated with simultaneously. This improves the speed at which memory is read/wrote to since this happens per clock cycle.

If you are running...

- single channel mode, it can transfer 64-bits of information per clock cycle
- [[#Dual Channel Mode|dual channel]] mode, 128-bits/clock cycle
- [[#Triple Channel Mode|triple channel]] mode, 192-bits/clock cycle

## Dual Channel Mode

To meet the demands of faster processors and memory controllers, the dual channel mode was developed so that the memory controller could interface with two [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMMs]] simultaneously. However these DIMMs must be identical.

In order for dual channel mode to function, the [[The Motherboard|motherboard]] must be equipped to work in dual channel mode, the [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMMs]] must be identical to each other in speed, size and features. The DIMMs must be inserted into the motherboard in a specific slot configuration.

![[Pasted image 20220824214533.png]]

[[The Motherboard|Motherboards]] will typically have color codings (see above image) to indicate to the user what order/places to place the [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMMs]].

## Triple Channel Mode

An uncommon method of communication with RAM is triple channel mode, where as the name suggests the memory controller has the ability to interface with 3 [[RAM Slots#Dual Inline Memory Module (DIMM)|DIMMs]] simultaneously.
