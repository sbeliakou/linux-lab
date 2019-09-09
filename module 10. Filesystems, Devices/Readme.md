## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks



1. Attach new hard drive to your CentOS VM using this [guide](https://www.techrepublic.com/article/how-to-add-new-drives-to-a-virtualbox-virtual-machine/) (up to "Preparing the drive for use" section)
2. Check which disks are mounted with `mount -a`
3. List disks by executiong `lsblk`. How do you think, which of them is disk that you just attached?
4. Disk without partitions under it is your new disk. Now, lets create two partitions on it:
  * List detailed info with `fdisk -l`
5. Create filesystem on your disk by running mkfs.ext4 /dev/[disk-name] 
6. Create new directory to mount your disk (for example, /opt1)
7. Mount disk by executing mount /dev/[disk-name] /opt1
8. Use df command again. Have your disk been successfully mounted?
9. Open /etc/fstab file. Add /dev/[disk-name] /opt1 ext4 defaults 0 0 to the end of it
10. Restart your system
11. Check df again. Have your disk been mounted automaticaly?
12. Copy some files to directory, where your disk is mounted
13. Unmount custom directory by running unmount /opt1. Do you have access to files that you copied before?
14. Remove your changes from fstab file
15. Format your disk with xfs filesystem
