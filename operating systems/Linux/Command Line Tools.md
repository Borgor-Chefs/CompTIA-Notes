---
tags:
  - os
  - linux
---

# Linux Command Line Tools

- `man`
   - opens up the manual of an binary if `man` has one
- `ls`
   - prints out the contents of a directory
- `pwd`
   - prints out the current working directory
- `mv <SRC> <DEST>`
   - moves a file, can also be used to rename a file
- `cp <SRC> <DEST>`
   - copies a file
- `rm <FILE>
   - deletes a file
- `rmdir <DIR>`
   - removes an empty directory, can also use `rm -rf <DIR>` to delete the directory and its contents
- `chmod <MODE> <FILE>`
   - this changes the permissions of a file, see [[#Ownership Octal]]
   - where `MODE` is `[ugoa][+|-][rwx]` or `0000` to `0777` (octal)
      - `u` is for user
      - `g` is for group
      - `o` is for other
      - `a` is for everyone
      - `r` is for read access
      - `w` is for write access
      - `x` is for execute access
      - `+` is to add a permission (if not exists)
      - `-` is to remove a permission (if not exists)
- `chown <owner:group> <FILE>
   - changes the ownership of a file
- `su` substitute user
   - you can become another user, although it's pretty much mainly used to swap to root
- `sudo` superuser do
   - execute commands as root
- `file`
   - describes a file to the user, the file type, attributes, notes about it
      - will say if a binary is stripped or not, dynamically linked or not
   - this relies on the magic bytes of a file
- `ip`
   - a huge command, used for networking
- `df` disk free
   - shows the amount of free space on the system, where the block is mounted, etc.
   - use `-h` for human-readable values e.g., gigabytes, megabytes, etc.'
- `grep PATTERN [FILE]`
   - matches pattern against strings either from a file or from STDIN
- `ps`
   - lists all currently running processes, their PID, state and what binary is associated with it
   - `ps aux` is probably the most useful since it will list ALL processes
- `top` (just install `htop`)
   - a better `ps` since it shows PID, user, memory usage, cpu usage, load and a bunch of other key information
- `find` finds a file
   - this is a very complex command but the basic usage is `find [DIR] -name [PATTERN]`
   - this command is extremely configurable but limited in what you want to do if you want to execute a command per file
- `dig`
   - lookup information from DNS servers, shows canonical names, IP addresses, cache timers, etc.
   - I don't think this is a default Linux utility, I've personally never heard of it before
- `cat ...` concatenates files
   - this program reads the contents of anything given to it and writes it to STDOUT
   - very useful for file manipulation along with pipelines
- `sed` stream editing
   - a powerful command whose sole purpose is to edit streams of text (using regular expressions)
- `nano` (you're a scrub if you use this, use `vim` instead)
   - a simple text editor that's usually installed with every single Linux distro
   - this is STUPID, install `vim` instead and be based
- `tar` stands for "Tape Archive"
    - this is the standard archiving utility with compression functionality (some algorithms will need their own standalone programs to be installed, this is just a wrapper program really)
- `rsync`
    - used for synchronizing files between computers, can be scheduled

## Ownership Octal

|#|Permission|Representation|
|-|-|-|
|7|Read, write, execute|`rwx`|
|6|Read and write|`rw-`|
|5|Read and execute|`r-x`|
|4|Read only|`r--`|
|3|Write and execute|`-wx`|
|2|Write only|`-w-`|
|1|Execute only|`--x`|
|0|None|`---`|

Given the format `?XXXYYYZZZ` of any file, the string is divided into 4 groups:

- `?` used to show special file attributes
   - if no special attributes, it will display as `-`
   - `B` for a block file (usually a storage medium found in `/dev`)
   - `C` for character file (usually a terminal or graphical display I'm pretty sure)
   - `L` for a symbolic link
   - `D` for a directory
   - `S` for a socket (networking, usually)
- `XXX` for the user permission octal
- `YYY` for the group permission octal
- `ZZZ` for the others permission octal
