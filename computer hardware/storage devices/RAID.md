---
tags:
  - storage
---
# Redundant Array of Independent Disks (RAID)

With data becoming more and more important, it becomes more important to ensure that the data doesn't get lost because of a [[HDD|hard drive]] failure. The solution to aid in the prevention of data loss is RAID.

Where RAID is a method of organizing data across [[HDD|hard drives]] to ensure that if one fails, nothing will be lost.

## Most Common Forms of RAID

There are many forms of RAID but the most common are;

- [[#RAID 0 (Striping)||RAID 0]] (striping)
- [[#RAID 1 (Mirroring)|RAID 1]] (mirror)
- [[#RAID 5 (Striping with Parity)|RAID 5]] (parity)
- [[#RAID 10 (RAID 1 & 0)|RAID 10]] (stripe of mirrors)
- [[#RAID 01 (RAID 0 & 1)|RAID 01]] (mirror of stripes)

### RAID 0 (Striping)

![[Pasted image 20220828164706.png]]

This form of RAID isn't actually RAID-like since it can decrease fault tolerance. This form of RAID involves splitting up or "striping" data across two disks. This decreases fault tolerance since if one disk fails, all data will be lost.

The read speed is the sum of all the read speeds of the disks running RAID 0

### RAID 1 (Mirroring)

![[Pasted image 20220828165232.png]]

RAID 1 is fault tolerant. In this setup, any data is copied onto another disk. So if one disk were to fail, you could use the backup disk and not have any set backs.

The downside to RAID 1 is that it is slower than [[#RAID 0 (Striping)|RAID 0]].

### RAID 5 (Striping with Parity)

![[Pasted image 20220828165549.png]]

In order to use RAID 5, you need to have 3 or more disks. In this setup, data is striped across multiple disks like in [[#RAID 0 (Striping)|RAID 0]], but unlike RAID 0 there are also parity partitions which are used to rebuild the data in case of a hard drive failure.

This is arguably the most common data setup for companies and storage centers. The only downside is that the total amount of storage will be less since an the equivalent of an entire disk is being used for parity data.

E.g., if you have four 1 TB disks (totally 4 TB), the effective amount of storage will be 3 TB since 1 TB will be used for parity data.

### RAID 10 (RAID 1 & 0)

![[Pasted image 20220828170122.png]]

RAID 10 requires a minimum of 4 disks. This setup combines [[#RAID 0 (Striping)|RAID 0]] then [[#RAID 1 (Mirroring)|RAID 1]] making RAID 10. RAID 0 splits incoming data into two different RAID 1 setups for data redundancy. This setup benefits from the fault tolerance of RAID 1 and the speed of RAID 0.

The only downside is that you can only use half the total storage since there are two disks that are duplicates of the other.

### RAID 01 (RAID 0 & 1)

![[Pasted image 20230508215724.png]]

RAID 01 requires a minimum of 3 disks (you'll most likely use 4). This setup combines [[#RAID 1 (Mirroring)|RAID 1]] then [[#RAID 0 (Striping)|RAID 0]] making RAID 01. RAID 1 mirrors data to each harddrive cluster which will then be striped across it using RAID 0.

This is considered a worse implementation when compared to [[#RAID 10 (RAID 1 & 0)|RAID 10]] since if two disks that contain the same data from both groups both fail, the system will fail.
