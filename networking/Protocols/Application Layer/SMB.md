---
tags:
  - networking
  - application_layer
---
# Server Message Block (SMB)

>[[Networking Ports|Standard port]]: SMB & CIFS 445
>[Link](https://en.wikipedia.org/wiki/Server_Message_Block).

>Latest version: 3.1.1 (Windows 10 & Windows Server 2016)

This is a protocol that enables file sharing, printer sharing, network browsing and inter-process communication (through named pipes) over a computer network. This is essentially a file sharing protocol, but the protocol is also capable of:

- dialect negotiation
- determining other SMB servers on a network (network browsing)
- printing over a network
- file, directory and share access auth
- file and record locking
- file and directory change notification
- extended file attribute handling
- unicode support
- opportunistic locks

This is an older protocol developed in 1983 by Barry A. Feigenbaum at IBM and relies on [[TCP]] for transport.

## Common Internet File System (CIFS)

This is a *dialect* of SMB and added more features such as:

- symbolic links
- hard links
- larger file sizes
- an attempt at direct connections over TCP port 445 without requiring a [[NetBIOS]] transport

This was Microsoft's attempt at renaming the protocol but ultimately failed, the features of this protocol were merged into SMB version 2.0 in 2006. From what I can tell, this protocol is still recognized but this is largely the same exact this as SMB, just with a different name.
