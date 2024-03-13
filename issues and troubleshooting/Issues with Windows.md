---
tags:
  - windows
  - os
  - issues
---
# Windows Troubleshooting

Here are some common errors and issues with Windows.

## BSOD/Frequent Shutdowns

This can be caused by multiple things:

- trying to access files you shouldn't
- Windows ran out of memory
- bad drivers
- bad hardware
- bad application

Tips to figure out what actually caused it:

- use last known good system restore if the problem is consistent
- rollback driver
- reset or remove hardware
- run hardware diagnostics
    - this is usually built into the [[The BIOS|BIOS]]

## Sluggish Performance

>This is usually how Windows operates ngl.

Things to check for:

- use [[Task Manager]] to see if any applications are using high CPU, I/O or RAM
- update Windows is generally a good idea
- check for disk space
- laptops will throttle CPU speed if the laptop is becoming too hot, you should check the fans too
- might be a [[!Malware|virus]]

## Boot Errors

These generally occur when the boot loader is incorrectly configured, generally happens when there are more than one operating system installed.

>I've also seen threads where Windows doesn't like sharing the same [[!Storage Devices|drive]] with other operating systems.

Here's what you should check:

- check that the boot configuration is actually correct

Here's what you can do to try and test what the problem is:

- remove any boot drives
- use Windows startup repair (if you can actually boot into the OS)
- modify the Windows Boot Configuration Database (BCD)

The command for that last one is `bootrec /rebuildbcd`.

>I believe that you can use something like System Rescue to repair the boot configuration, but I'm not sure nor have I done this.

## Startup Repair

The main keyword is "Missing NTLDR", this means that the boot loader is **missing**. I really don't know how one would do this unless you're really fucking around.

Two things to try and fix it:

- run Startup Repair
- manually replace the boot loader and reboot
    - this is done by copying the files from a good windows installation into the bad one
- disconnect any boot drives
- boot into Safe Mode

This might also fix [[#Boot Errors|a missing operating system]] error.

## Hardware Not Working Properly

Sometimes hardware won't work correctly, but you can check the status of hardware with both [[Device Manager]] and [[Event Viewer]].

In device manager, you can update and check the driver for a specific piece of hardware.

In event viewer, you can try and piece together what's going on or why this piece of hardware is failing.

### "One or more services failed to start"

This is usually caused by a bad or incorrect driver or bad hardware. To fix this you can:

- try starting the service manually
- check account permissions
- confirm service dependencies
    - if it's a Windows service, check the system files
    - if it's an application, try reinstalling it

## Applications Crashing

Sometimes, an application will just stop working, it may or may not provide an error message or it may just disappear.

To investigate, use the [[Event Viewer]], specifically the logs for this application. You can also check the "Reliability Monitor" (in the control panel under "Security and Maintenance") to check for a history of application problems, it apparently also checks for resolutions.

A quick final fix is just to reinstall.

## Low Memory Warnings

Some applications are nice and memory efficient, some are bloated piles of shit that need to be burned with fire and completely rewritten. Here are some solutions:

- simply get more [[RAM]]
- close processes that are hogging too many resources
- increase the amount of virtual memory

>The setting for virtual memory is in "System > About > Advanced System Settings > Performance > Settings > Virtual Memory". This is where Windows will use some of your storage drive for RAM.

## USB Controller Resource Warnings

So USB controllers manage your USB devices, all controllers have buffers called "endpoints" which are assigned to each device. What can happen is that a particular USB device will use too many endpoints for the specific version of USB port you have or you might just run out.

It's apparently, really hard to know how many endpoints a specific USB device uses so you're better off working around this.

Some work arounds for this are:

- move the device to a different USB interface
- match the USB interface to the device capabilities i.e., match USB 2.0 with 2.0 and 3.0 with 3.0

>You might be able to buy a USB hub to get around but I'm not sure how this would work, I've never personally experienced this issue.
