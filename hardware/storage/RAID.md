Tags: [#storage]

# Redundant Array of Independent Disks (RAID)

With data becoming more and more important, it becomes more important to ensure that the data doesn't get lost because of a [[HDD|hard drive]] failure. The solution to aid in the prevention of data loss is RAID.

Where RAID is a method of organizing data across [[HDD|hard drives]] to ensure that if one fails, nothing will be lost.

## Common Forms of RAID

There are many forms of RAID but the most common are;

- [[#^e97b0e|RAID 0]]
- [[#^16a520|RAID 1]]
- [[#^627352|RAID 5]]
- [[#^991c01|RAID 10]]

### RAID 0 (Striping)

^e97b0e

![[Pasted image 20220828164706.png]]

This form of RAID isn't actually RAID-like since it can decrease fault tolerance. This form of RAID involves splitting up or "striping" data across two disks. This decreases fault tolerance since if one disk fails, all data will be lost.

The only advantage to RAID 0 is speed since you have two independent disks running at the same time.

### RAID 1 (Mirroring)

^16a520

![[Pasted image 20220828165232.png]]

RAID 1 is fault tolerant. In this setup, any data is copied onto another disk. So if one disk were to fail, you could use the backup disk and not have any set backs.

### RAID 5 (Striping with Parity)

^627352

![[Pasted image 20220828165549.png]]

In order to use RAID 5, you need to have 3 or more disks. In this setup, data is striped across multiple disks like in [[#^e97b0e|RAID 0]], but unlike RAID 0 there are also parity partitions which are used to rebuild the data in case of a hard drive failure.

This is arguably the most common data setup for companies and storage centers. The only downside is that the total amount of storage will be less since an the equivalent of an entire disk is being used for parity data.

E.g., if you have four 1 TB disks (totally 4 TB), the effective amount of storage will be 3 TB since 1 TB will be used for parity data.

### RAID 10 (RAID 1 & 0)

^991c01

![[Pasted image 20220828170122.png]]

RAID 10 requires a minimum of 4 disks. This setup combines [[#^e97b0e|RAID 0]] and [[#^16a520|RAID 1]] making RAID 10. RAID 0 splits incoming data into two different RAID 1 setups for data redundancy. This setup benefits from the fault tolerance of RAID 1 and the speed of RAID 0.

The only downside is that you can only use half the total storage since there are two disks that are duplicates of the other.
