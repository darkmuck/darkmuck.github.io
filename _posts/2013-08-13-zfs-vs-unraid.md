---
ID: 1951
post_title: ZFS vs unRAID
author: Shwuzzle
post_date: 2013-08-13 21:24:00
post_excerpt: ""
layout: post
published: true
---
If you are looking for a good solution to protect your data, but want it to be more flexible than something like a RAID 1 or RAID 5 you may have considered ZFS, unRAID, or various other proprietary solutions.

ZFS is a combined file system and logical volume manager (LVM) originally created by Sun Microsystems. It is now open source and comes with Solaris-based and BSD-based operating systems. In addition, it can be installed on Linux with a bit of extra work. ZFS is able to provide support for extremely large storage capacities, snapshots, continuous integrity checking, automatic repair, volume management, and more. ZFS was designed from the ground up to be a completely new concept in regards to how filesystems have traditionally been designed.

unRAID Server is an operating system that boots from a USB flash drive and is designed to be a Network Attached Storage (NAS) operating system. It has some features of RAID 5 but it also has quite a few differences. It uses a dedicated parity drive instead of parity being striped across all drives. You can add a cache drive for extra performance. unRAID can recover from single drive failures and still have the ability to access the data (due to parity drive). A failed drive can be fully rebuilt based on the parity drive. Overall performance is a bit slower than RAID 5, but the benefits can outweigh the performance cost for certain use cases; most notably something like media storage.

How do these two solutions compare? ZFS wins in terms of features and possibly performance. ZFS, unlike unRAID, allows you to add extra disks of any size dynamically, integrated compression, dynamic striping, snapshots, encryption, and a whole lot more. ZFS can also be used in combination with a RAID setup. Thereby providing a few extra things. However, it's recommended to use only a Software RAID instead of Hardware RAID, because with Hardware RAID ZFS will always detect all data corruption but won't be able to repair it because the hardware RAID will interfere and ZFS won't be able to prevent it. ZFS can also be used on just about any Unix (Solaris) or Unix-like (BSD, Linux) system. unRAID is more of an all-in-one solution; in that it provides a standalone operating system that is bootable via USB flash disk. This is extremely useful because of the ease of installation, easy recovery from disk failure, fairly good performance, and existence of parity on a totally separate standalone device.

Personally I would be most inclined to choose ZFS for its flexibility and feature set. It is a great file system overall but it can sometimes be a bit difficult to configure. If its not configured correctly IOPS performance can suffer, especially if one a single group of disks is configured as a single vdev. In this single configuration, performance would be limited to the speed of the slowest disk in the pool. However, with a bit of practice and learning you can get some good performance out of it.

More Information:
<ul>
	<li><a href="http://en.wikipedia.org/wiki/ZFS">ZFS (wikipedia.org)</a></li>
	<li><a href="http://lime-technology.com/wiki/index.php/UnRAID_Wiki">unRAID - Wiki (lime-technology.com)</a></li>
</ul>
