## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)
  
## Tasks

1. Attach new 2GB hard drive to your CentOS VM using [this guide](https://www.techrepublic.com/article/how-to-add-new-drives-to-a-virtualbox-virtual-machine/) (up to "Preparing the drive for use" section)

2. List disks by executing `lsblk`. How do you think, which of them is disk that you just attached?

3. Disk without partitions under it is your new disk. Now, lets create the first partition on it:
    * List detailed info with `fdisk -l`
    * Go to interactive mode by running `fdisk /dev/[disk-name]`
    * In the interactive mode, type `p` and hit Enter to see current partitions. Is there anything now?
    * Type `n` to create new partition
    * Use `p` to set primary partition
    * Leave partition number and first sector with the default values (just hit Enter)
    * Set last sector to +1G
    * Check current partitions again. What have changed?
    * Type `w` to save your partition
  
4. Create the second primary partition with all options set to default

5. List info about partitions again. What size does your second partition have?

6. Update partitions by running `partprobe /dev/[disk-name]`

7. Create filesystem on your first partition by running `mkfs.vfs /dev/[disk-name][part-number]`

8. Create filesystem on your second partition

9. Create 2 new directories to mount your disk (for example, /opt1 and /opt2)

10. Mount first partition by executing `mount /dev/[disk-name][part-number] /opt1`

11. Mount second partition to /opt2

12. Use command `df -HT`. Have your disk been successfully mounted? What filesystem does it have?

13. Open /etc/fstab file. Add `/dev/[disk-name][part-numbet] /opt1 xfs defaults 0 0` to the end of it

14. Add second partition to `/etc/fstab`

15. Restart your system

16. Check df again. Have your disk been mounted automaticaly?

17. Copy `/etc/filesystems` to /opt1 and /opt2

18. Change directory to /opt2

19. Try to unmount directory with `umount /opt2`. What happened?

20. Return to your home directory and unmount /opt2. Do you have access to file that you copied before?

21. Remove your second partition from fstab file

22. Delete your second partition:
    * Run `fdisk /dev/[disk-name]`
    * List partitions
    * Type `d`
    * Enter number of partition to delete
    * To confirm deletion, type `p` and then type `w`

23. Update partitions by running `partprobe /dev/[disk-name]`

24. Run `fdisk -l`. What have changed?

