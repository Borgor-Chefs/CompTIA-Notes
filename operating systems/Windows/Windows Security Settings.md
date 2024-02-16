---
tags:
  - os
  - windows
  - security
---
# Windows Security Settings

## NFTS v.s. Share Permissions

![[Pasted image 20240216155007.png]]

>On the left shows [[File Systems#File System Types|NTFS]] permissions, on the right, share permissions.

For every file and folder on an [[File Systems#File System Types|NTFS]] filesystem have a set of permissions that dictate what users can and cannot do. But, for users connecting over a network there's a different set of permissions.

There are times when these settings overlap, in order to resolve this, the most restrictive setting takes priority i.e., if the share has full access but the [[File Systems#File System Types|NTFS]] drive has read-only, a user accessing this drive will only be allowed to read the files, not write nor execute.

Finally, with [[File Systems#File System Types|NTFS]], permissions are inherited from their immediate owner.

## User Account Control (UAC)

![[Pasted image 20240216155239.png]]

This is sliding bar that changes how Windows will behave when informing you of events that happen on your computer. The two things that Windows will notify you about is when:

- applications make changes to the computer
- someone modifies Windows settings
