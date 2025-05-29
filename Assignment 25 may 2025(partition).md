1. Create a New Partition with ext3 Filesystem
   a.Identify an available disk >>fdisk -l(cmnd)
   b.Create a new partition >> 1. fdisk /dev/sda 
                               2.n (new partition) >>/dev/sda4 created.
                               3. +250M (size of new partition)
                               4.p(for listing the partitions)
                               5.W(saving the changes)
   c.Format the new partition with the ext3 filesystem>> mkfs.ext3 /dev/sda4 
2.Mount the Partition to /mnt/partition
 a.Create the mount point directory>>mkdir /mnt/partition
 b.Mount the partition to /mnt/partition>>1.vim /etc/fstab
                                          2./dev/sda4 /mnt/pattition ext3 default 0 0
                                          3.:wq
