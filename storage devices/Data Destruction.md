---
tags:
  - storage
  - os
---
# Data Destruction

Here are some methods you can use to thoroughly destroy data:

- [[#Physical Destruction]]
- [[#Physical Destruction]]
- [[#Third Party Destruction]]
- [[#Disk Formatting]]
- [[#Erasing Individual Files]]

It's always a good idea to format your drives before giving them away or selling them because you never know what information about you or important, sensitive information might be on that device.

## Physical Destruction

- an industrial shredder
    - this is heavy machinery, [[HDD]] or [[SSD]] goes in and tiny little bits come out
- a drill or hammer
    - quick and easy
    - take out the platters from an [[HDD]] and either smash or drill them
    - drill or smash the chips on an [[SSD]]
- electromagnetic (degaussing)
    - remove the magnetic field from the device
    - this will destroy the data and the electronics too
- incineration
    - fire is hot.

## Third Party Destruction

This is where you outsource destroying your data and or devices to another company and they will give you some sort of verification or certificate that whatever you gave them was destroyed.

## Disk Formatting

There are three options here:

- low-level formatting
    - this is apparently something done by the manufacturer and isn't available to people outside of the factory
- quick formatting
    - this is where you remove the first (I believe) 512 or 1024 bytes of the drive **but** this will leave the rest of the data on the drive intact.
    - in practice, Windows or Linux will notice that the drive is fresh/new and ask if you want to make a file system, when you say yes the OS will create a new [[File Systems|FS]] on the drive and treat it like there is nothing there
- regular formatting
    - this is where you completely wipe the device clean, change every bit to a zero so that the entire device is zero'd out, no data remains
    - you will **not** be able to recover your data here

If you want to erase everything without being able to recover any data at all, choose the regular format. If you just want to start anew and don't care about what's on the drive, choose quick or standard.

You can also use something like DBAN a.k.a. Darik's Boot and Nuke that wipes the device as many times as you would like.

## Erasing Individual Files

There are tools like `sdelete` from Windows that can securely delete files from your drive. With Windows specifically, when you delete a file, the file gets moved to a "hidden" partition of your drive, this is the Recycle Bin.

Using `sdelete` will actually delete the file and not just move the file somewhere else.

>At least that's what it's supposed to do.
