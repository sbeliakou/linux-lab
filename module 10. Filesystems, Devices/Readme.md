## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

### 1. Add new hard drive to VM

#### Add disk

- Attach new 2GB hard drive to your CentOS VM using [this guide](https://www.techrepublic.com/article/how-to-add-new-drives-to-a-virtualbox-virtual-machine/) (up to "Preparing the drive for use" section)

- List disks by executing `lsblk`. How do you think, which of them is disk that you just attached?

#### Create partition

- Disk without partitions under it is your new disk. Now, lets create the first partition on it:
    * List detailed info with `fdisk -l`
    * Go to interactive mode by running `fdisk /dev/[disk-name]`
    * In the interactive mode, type `p` and hit Enter to see current partitions. Is there anything now?
    * Type `n` to create new partition
    * Use `p` to set primary partition
    * Leave partition number and first sector with the default values (just hit Enter)
    * Set last sector to +1G
    * Check current partitions again. What have changed?
    * Type `w` to save your partition

- Create the second primary partition with all options set to default

- List info about partitions again. What size does your second partition have?

- Update partitions by running `partprobe /dev/[disk-name]`

#### Mount partitions 

- Create filesystem on your first partition by running `mkfs.vfs /dev/[disk-name][part-number]`

- Create filesystem on your second partition

- Create 2 new directories to mount your disk (for example, /opt1 and /opt2)

- Mount first partition by executing `mount /dev/[disk-name][part-number] /opt1`

- Mount second partition to /opt2

- Use command `df -HT`. Have your disk been successfully mounted? What filesystem does it have?

#### Enabling automount

- Open /etc/fstab file. Add `/dev/[disk-name][part-numbet] /opt1 xfs defaults 0 0` to the end of it

- Add second partition to `/etc/fstab`

- Restart your system

- Check df again. Have your disk been mounted automaticaly?

### 2. Working with partitions

- Copy `/etc/filesystems` to /opt1 and /opt2

- Change directory to /opt2

- Try to unmount directory with `umount /opt2`. What happened?

- Return to your home directory and unmount /opt2. Do you have access to file that you copied before?

- Remove your second partition from fstab file

- Delete your second partition:
    * Run `fdisk /dev/[disk-name]`
    * List partitions
    * Type `d`
    * Enter number of partition to delete
    * To confirm deletion, type `p` and then type `w`

- Update partitions by running `partprobe /dev/[disk-name]`

- Run `fdisk -l`. What have changed?


## Helpful Materials
- https://www.youtube.com/watch?v=_h30HBYxtws
- https://www.youtube.com/watch?v=KfiFsUCntGM&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=43
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/deployment_guide/ch-disk-storage
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/deployment_guide/chap-using_the_mount_command
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/deployment_guide/ch-swapspace
- https://codingbee.net/rhcsa/rhcsa-overview-of-partitions-and-logical-volumes
- https://codingbee.net/rhcsa/rhcsa-creating-partitions
- http://www.tldp.org/LDP/sag/html/filesystems.html#FS-INTRO
- https://linuxsurvival.com/linux-tutorial-introduction/
- https://linuxjourney.com/lesson/filesystem-hierarchy
- https://linuxjourney.com/lesson/device-types
