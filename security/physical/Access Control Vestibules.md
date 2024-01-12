# Access Control Vestibules

These are systems to control a person's access, usually through a series of locked doors. These doors are (usually) electronically operated and can be controlled and accessed remotely.

## System Types

While there aren't names for these (that I found), here are some common systems that the doors are managed by:

- all doors unlocked
    - in this setting, all associated doors are unlocked until a door is opened which makes all other doors locked until the opened door is closed
- all doors locked
    - unlocking one door (by some form of authentication), prevents any other associated door from unlocking until the opened door is closed and relocks itself
- one door open, all others locked
    - this is similar to the previous however, there is one unlocked door that a person can enter through
    - when this unlocked door is opened, all the other doors are prevented from being unlocked until the entry door is closed

The goal of this is to, ideally, control only one person from entering this essentially buffer room at a time. The idea is to put any given person into said buffer room, force them to provide authentication to go further into the facility or reject them.

## Typical Authentication Types

You would have one or more of the following for authentication:

- keys (like lock and key)
- [[Badge Reader|badge reader]] (either something like a credit card or a badge)
    - [[NFC|NFC]]
    - [[RFID|RFID]]
    - magnetic swipe (think credit card swipe)
- pin machines with a keyboard
- biometric security
    - fingerprint reader
    - retinal scan
- human security (security guards)

There can be a combination of the above, say a pin machine & keycard reader built into one where:

- you enter a pin
- you swipe or tap a card
- you both of the above
