---
tags:
  - networking
---
# Ethernet Standards

There are different types of **copper** cables with varying speeds and physical properties, namely the tightness of the twists applied to the wires.

The "BASE" in all of the standards refers to "baseband", meaning that there is a single frequency of EM being sent over the wire. Broadband means many frequencies that share the single medium.

## Copper Cable Standards

>See more about copper cables [[Digital Cables|here]].

| Ethernet Standard | Cable Category | Speed (Mbps) | Maximum Supported Distance (meters) | Notes                        |
| ----------------- | -------------- | ------------ | ----------------------------------- | ---------------------------- |
| 10BASE-T          | 3              | 10           | 100                                 | No longer used.              |
| 100BASE-TX        | 5              | 100          | 100                                 | No longer used.              |
| 1000BASE-T        | 5              | 1,000        | 100                                 | No longer used.              |
| 1000BASE-T        | 5e (enhanced)  | 1,000        | 100                                 |                              |
| 10GBASE-T         | 6              | 1,000        | Unshielded: 55, Shielded: 100       | Uses a frequency of 500 MHz. |
| 10GBASE-T         | 6a (augmented) | 10,000       | Shielded or unshielded:100          |                              |
| 10GBASE-T         | 7              | 10,000       | 100                                 | Shielded cables only.        |
| 40GBASE-T         | 8              | 10,000       | 30                                  | Shielded cables only.        |

>The 10G and 40G mean "gigabit", otherwise it's "megabit".

The standards 10BASE-T and 100BASE-TX were made to use two pairs of wires in an [[Cable Standards|ethernet cable]], the newer standards use all 4 pairs. Some older [[Patch Panel|patch panels]] and [[Punch Down Interface|punch down interfaces]] only have space for two pairs of wires, if you try to use a 4-pair cable in this type of block, you won't be able to get gigabit speeds.

## Fiber Cable Standards

>See more about fiber optic cables [[Fiber Optic Cables|here]].

| Ethernet Standard | Cable Medium             | Speed (Mbps) | Maximum Supported Distance                       | Notes                         |
| ----------------- | ------------------------ | ------------ | ------------------------------------------------ | ----------------------------- |
| 100BASE-FX        | Multi-mode fiber         | 100          | 400 (half-duplex)<br>2 km (full-duplex)          | Uses laser components         |
| 100BASE-SX        |                          | 100          | 300                                              | Uses LEDs                     |
| 1000BASE-SX       | Usually multi-mode fiber | 1,000        | 220 to 550 depending on the type of fiber.       | Uses a short wavelength laser |
| 1000BASE-LX       |                          | 1,000        | Multi-mode fiber: 550<br>Single-mode fiber: 2 km | Uses a long wavelength laser  |
| 10GBASE-SR        | Multi-mode fiber         | 10,000       | 26 to 400                                        | Short range                   |
| 10GBASE-LR        | Single-mode fiber        | 10,000       | 10 km                                            | Long range                    |
