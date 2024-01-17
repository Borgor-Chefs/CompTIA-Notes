---
tags:
  - os
  - macos
  - utility
---
# XProtect

Apple uses their own application XProtect to analyze program signatures and files to see if they contain any known malware signatures. This database of signatures is updated regularly, I'm assuming XProtect makes a connection to some centralized Apple database of malware signatures and fetches it periodically.

XProtect checks for known malicious content whenever:

- an app is first launched
- an app has been changed (in the file system)
- XProtect signatures are updated

Whenever XProtect detects malware, the software is immediately blocked, the user is notified of this and is given the option to move the software into the trash. 

>Apple says that XProtect's methods are more "generic" than just file hashes, allowing it to detect malware that it hasn't even seen yet.  
>Not sure what this means or entails.

XProtect will occasionally scan your system for malware and gets updates from Apple itself whenever you decide to update the system.
