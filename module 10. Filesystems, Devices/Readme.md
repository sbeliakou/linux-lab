## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks



Attach new hard drive to your CentOS VM using the guide below (up to "Preparing the drive for use" section)
https://www.techrepublic.com/article/how-to-add-new-drives-to-a-virtualbox-virtual-machine/
Check which disks are mounted with mount -a
List disks by executiong ls /dev. How do you think, which of them is disk that you just attached?
Check disks partitions by running df. Partitions have naming convention /dev/[disk-name][number], so that disk without partition is your new disk. Check your assumption 
Create filesystem on your disk by running mkfs.ext4 /dev/[disk-name] 
Create new directory to mount your disk (for example, /opt1)
Mount disk by executing mount /dev/[disk-name] /opt1
Use df command again. Have your disk been successfully mounted?
Open /etc/fstab file. Add /dev/[disk-name] /opt1 ext4 defaults 0 0 to the end of it
Restart your system
Check df again. Have your disk been mounted automaticaly?
Copy some files to directory, where your disk is mounted
Unmount custom directory by running unmount /opt1. Do you have access to files that you copied before?
Remove your changes from fstab file
Format your disk with xfs filesystem
