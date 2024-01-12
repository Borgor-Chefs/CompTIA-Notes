Tags: [#networking #application_layer]
[[Standard Ports|Standard port]]: 20/21
[Link](https://en.wikipedia.org/wiki/File_Transfer_Protocol).

# FTP (File Transfer Protocol)

This is the standard protocol used by web users for file transfer. Users can download and upload files over the internet. This transfer can be done by a web browser or FTP software.

This is a connection oriented protocol that uses [[TCP|TCP]] for the actual file transfer.

![[Pasted image 20230331193547.png]]

## Variations

The following protocols are based off of FTP but are different in their own right.

### TFTP (Trivial File Transfer Protocol)

This is a very simple protocol that is similar to FTP but also very different:

- this isn't used over the internet but rather over the same network
- used for transferring files over the same network
- this uses [[UDP|UDP]] instead of [[TCP|TCP]]

### SFTP (Secure/SSH File Transfer Protocol)

This is again similar to [[FTP|FTP]] however this protocol adds a layer of security by using SSH.
