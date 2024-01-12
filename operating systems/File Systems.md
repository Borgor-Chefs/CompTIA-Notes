Tags: [#os]

# File Systems

Before data can be written to your storage device, the device must first be partitioned and given structure before anything can be written to it. Operating systems expect the data to be written in a certain format.

- [[#File System Types|list of file system types]]
- [[#File System Formatting|file system formatting]] (resetting/deleting file systems)

## File System Types

Formats such as:

- the File Allocation Table (FAT) family
	- FAT
		- released in 1980
	- FAT32
		- can support a 2 TB storage device
		- maximum file size of 4 GB
	- exFAT
		- compatibility with most operating systems
	- VFAT
- NTFS
	- the parent file system for this one is FAT32
	- many operating systems support reading NTFS, but not writing
	- this is mainly for [[Overview|Windows]], notable features include
		- quotas
		- file compression
		- encryption
		- symbolic links
		- large file support
		- security
		- recoverability
- the Extended File System (EXT) family
	- EXT3
		- commonly used by [[Operating Systems Overview#Linux|Linux]]
	- EXT4
		- commonly used by Linux and [[Operating Systems Overview#Google Android|Android OS]]
- ReFS
	- this is also mainly for [[Overview|Windows]]
- APFS
	- this is exclusive to [[Operating Systems Overview#Apple|Apple]] devices and has been optimized for SSDs
	- notable features include
		- encryption
		- snapshots
		- better data integrity

## File System Formatting

This is a way of creating or rewriting the file system, this can be good or bad in some scenarios.

- quick format
	- this just creates a new file table
	- it looks like the data on the device has been erased but it is simply just invisible to the OS with the new, empty file table
	- no additional checks are made
- full format
	- this flips every single bit on the device to a zero
	- this makes all saved data on the device unrecoverable as it as been expunged from the drive
	- also checks the disk for bad sectors (quite time consuming)

>Quick format is the default format used during the installation of [[Windows Editions|Windows 10 and 11]].
>The Windows command `diskpart` can be used for a full format.

>A handy command to do this on [[Operating Systems Overview#Linux|Linux]] is:
>`dd -if /dev/zero -of /dev/[hard drive]`
>Here, you are echoing zeros into the targeted [[certifications/comptia a+/hardware/storage/About|hard drive]].
