---
tags:
  - networking
---
# Radio-Frequency Identification (RFID)

>This technology uses [electromagnetic fields](https://en.wikipedia.org/wiki/Electromagnetic_field "Electromagnetic field") to automatically [identify](https://en.wikipedia.org/wiki/Automatic_identification_system "Automatic identification system") and [track](https://en.wikipedia.org/wiki/Tracking_system "Tracking system") tags attached to objects. An RFID system consists of a tiny radio [transponder](https://en.wikipedia.org/wiki/Transponder "Transponder"), a [radio receiver](https://en.wikipedia.org/wiki/Radio_receiver "Radio receiver") and [transmitter](https://en.wikipedia.org/wiki/Transmitter "Transmitter"). When triggered by an electromagnetic interrogation pulse from a nearby RFID reader device, the tag transmits digital data, usually an [identifying inventory number](https://en.wikipedia.org/wiki/Identifier "Identifier"), back to the reader. This number can be used to track [inventory](https://en.wikipedia.org/wiki/Inventory "Inventory") goods.
>From [Wikipedia](https://en.wikipedia.org/wiki/Radio-frequency_identification)

## Example Card

![[Pasted image 20231218172043.png]]

The above image is an example of a RFID card, wherein the orange wire is an antenna and the brown-ish rectangle is a RFID chip. This chip should contain a unique identifier that no one else has.

>Now, the vulnerability here is if someone has a device to read the signal emitted from one of these cards and copy it. Now, this same person could create a new card with your RFID signature and use it to bypass security checks.
>
>The issue with this is the implementation of the security system, as there could be many more layers to it. If you were to use a cloned card as a skeleton key and it doesn't work, it could trigger an alarm or something else.
>
>Also, it really depends on the implementation of the card itself and the technology being used. There could be multiple steps to achieve entry or the actual implementation of the card itself could be customized e.g., vendor specific.
