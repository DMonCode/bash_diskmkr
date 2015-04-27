# bash_diskmkr

Disk Maker
==========

This is BETA.
You should probably not use this with out testing it first
I use it for a particular use case.
It works for that use case.
I make no gurantee it will work for your use case. 

Echoing to fdisk is fun.
But it is beta so be careful.

-----------------------


Bask disk maker is a simple script that:

1. Takes a new drive and adds it to the volume group.
2. Resizes logical volume to take up full size of disk
3. Resizes file system to make use of new space.

This script is not structured around using partial disks.

Usage
----

 - h  Display Help
 - a  Add disk [Currently not working: This is a future thought that I haven't gotten around to]
 - e  Extend disk
 - d  Directory you will mount the disk to. [Currently disabled: I tend to use puppet to ensure the actual mount.]
 - g  Volume Group (VG) that disk will be added to.
 - l  Logical Volume (LV) that will be extended
 - p  Physical Volume (PV) that will be added

Example:

After adding a new disk you want to add it to the volume group for /var

diskmkr -e -p /dev/sdb -g VGvar -l LVvar -d /var


