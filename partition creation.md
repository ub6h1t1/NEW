Create a New Partition with ext3 Filesystem

Identify an available disk (e.g., /dev/sdb)--->df -h
Create a new partition (e.g., /dev/sdb1)---->sudo fdisk /dev/sda4
Format the new partition with the ext3 filesystem
**********************
root@beema:~# mkfs.ext3 /dev/sda4
mke2fs 1.47.0 (5-Feb-2023)
Creating filesystem with 2358528 4k blocks and 589824 inodes
Filesystem UUID: e628ec65-c4c4-4d48-bef7-fde11749395b
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632

Allocating group tables: done
Writing inode tables: done
Creating journal (16384 blocks): done
Writing superblocks and filesystem accounting information: done
***new directory created as grapes*************
root@beema:~# mkdir /grapes
**********mounting /dev/sda4 in to /grapes************
root@beema:~# mount /dev/sda4 /grapes
root@beema:~# df -h
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           197M  1.1M  196M   1% /run
/dev/sda2        15G  4.9G  9.1G  35% /
tmpfs           985M     0  985M   0% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
/dev/sda3       974M  124K  907M   1% /home
tmpfs           197M   12K  197M   1% /run/user/1000
/dev/sda4       8.8G   92K  8.4G   1% /grapes
***change directory******
root@beema:~# cd /grapes
***file created on /grapes****
root@beema:/grapes# vim adres
**content of file adres****
root@beema:/grapes# cat adres
this is my address
ABCD house
34block,
near palarivattom,ernakulam
root@beema:/grapes#



