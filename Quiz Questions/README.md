# Quiz
 
## module 01. What Linux Is
## module 02. Linux Family
Select correct statements:
- [x] Linux is inexpensive and powerful alternative to other OS
- [ ] Linux doesn't support multi-user and multitasking technologies
- [x] Linux runs on a variety of platforms
- [x] Linux is developed by Linus Tordvalds in July 1991
  
Select Linux features:
- [ ] Insecure (prone to common vulnerabilities associated with Windows)
- [x] Open source (code freely available)
- [ ] Expensive (can be downloded only for money)
- [x] Higher stability than other OSes
  
Does Open Source mean free access to source code - right to modify without restriction, right to freely distribute software?
- [x] True
- [ ] False

## module 03. CentOS Installation and Basic Configuration
## module 04. Basic Shell Usage

How does bash standart prompt look like?
- [ ] >
- [x] $
- [ ] /
- [ ] #

How to get to the directory, which is two levels upper?
- [ ] cd ./[2]
- [ ] cd -
- [ ] cd ../
- [x] cd ../..

How to find, in which directory are you now?
- [x] pwd
- [ ] whereami
- [ ] echo $HOME
- [ ] echo $PATH

How to list content of the directory in reverse order?
- [x] ls -r
- [ ] ls -R
- [ ] ls -l
- [ ] ls -s

How to find info about all `mv` command options?
- [x] man mv
- [x] mv --help
- [x] info mv
- [ ] options mv 

How to clear terminal?
- [ ] purge
- [ ] clean
- [x] clear
- [x] Ctrl+l

How to find list of all performed commands?
- [x] history
- [ ] cat /etc/history
- [ ] cat /home/user/.bash_history
- [ ] cat $(echo $HISTFILE)

## module 05. Linux Directories Layout
Which of the following command shows you current time?
- [ ] whoami
- [ ] cd time
- [x] date
- [ ] pwd

How to get the current directory?
- [ ] print directory
- [ ] getworkdir
- [x] pwd
- [ ] echo dir

How to get the current directory content as list view?
- [ ] Get-Content
- [x] ls -l
- [ ] pwd
- [x] ls -al

You were in /home/user - your home directory. Then you went to /home/user/subfolder directory. How you can come back to /home/user?
- [x] cd
- [x] cd ..
- [x] cd -
- [x] cd ../../user

## module 06. Working with Files
How to create new directory?
- [x] mkdir new_dir
- [ ] touch new_dir
- [ ] echo "new_dir" >
- [x] mkdir -p new_dir/new_sub_dir

How to create new file?
- [x] touch new_file
- [x] vi new_file
- [ ] mkdir new_file
- [x] echo "new_file" > new_file

How save file and exit from vi?
- [ ] :q!
- [ ] ctrl+o
- [ ] ctrl+x, ctrl+c
- [x] :wq

How to append line to the end of non-empty file?
- [ ] append "line" file1
- [ ] echo "line" > file1
- [ ] add "line" file1
- [x] echo "line" >> file1

How to print last 10 lines of file?
- [ ] print -l {-10..} file
- [x] tail file
- [x] tail -n 10 file
- [ ] head -n 10 file

How to print first 10 lines of file?
- [ ] print -l {0..10} file
- [x] head file
- [x] head -n 10 file
- [ ] tail -n 10 file

How to rename file?
- [ ] cp file1 file2
- [ ] rn file1 file2
- [x] mv file1 file2
- [ ] rm file1 file2

How to copy file?
- [x] cp file1 file2
- [ ] rn file1 file2
- [ ] mv file1 file2
- [ ] rm file1 file2

How to remove files?
- [ ] cp file1 file2
- [ ] rn file1 file2
- [ ] mv file1 file2
- [x] rm file1 file2

How to archive folder?
- [ ] arch folder1 folder.zip
- [x] tar -czvf myarchive.tar.gz folder1/
- [ ] tar -tvf myarchive.tar.gz
- [ ] tar -xzvf myarchive.tar.gz

How to unarchive folder?
- [ ] arch folder1 folder.zip
- [ ] tar -czvf myarchive.tar.gz folder1/
- [ ] tar -tvf myarchive.tar.gz
- [x] tar -xzvf myarchive.tar.gz


How to explore the content of archive?
- [ ] arch folder1 folder.zip
- [ ] tar -czvf myarchive.tar.gz folder1/
- [x] tar -tvf myarchive.tar.gz
- [ ] tar -xzvf myarchive.tar.gz

How to find `myfile` file?
- [x] locate myfile
- [x] find / -name "myfile" -type f
- [ ] search myfile
- [ ] where myfile

## module 07. Linux Users and Groups
How to create group with custom gid?
- [ ] groupadd group_name
- [x] groupadd group_name -g 1250
- [ ] create group 1250
- [ ] newgroup group_name -gid 1250

How to create user and assign him to group1?
- [x] useradd -g group1 -G group1 user1
- [ ] useradd user1
- [ ] useradd user1 group1
- [ ] assign -u user1 -g group1

How to switch to user2?
- [x] su - user2
- [x] su user2
- [ ] su
- [ ] login user2

## module 08. File Permissions, Links
Identify the following permissions: -rwxrw-r--
- [ ] Read, write and execute by everyone, read and write for group members and read only for the owner
- [x] Read, write and execute by owner, read and write for group members and read only for everyone else
- [ ] Read, write and execute by group members, read and write for the owner and read only for everyone else
- [ ] Read, write and execute by group members, read only for owner and read and write for everyone else

Select the right octal equivalents for the permissions
- [x] -rwxrw-r-- = 764
- [ ] -rw------- = 500
- [x] -rwxrw-r-x = 765
- [ ] -rw-r--r-- = 655
- [x] -r-------- = 400

How to create symlink to the /home/folder1?
- [ ] cp -r /home/folder1 mylink
- [x] ln -s /home/folder1 mylink
- [ ] mv -f /home/folder1 mylink

What links are bigger?
- [ ] symlink
- [x] hardlink

Does file movement affect soft link?
- [x] affect
- [ ] doesn't affect

## module 10. Filesystems, Devices
What utilites you will use to manage disks in CentOS?
- [x] df
- [ ] dd
- [x] fdisk
- [x] partprobe

How to receive detailed info about disks partitions?
- [x] fdisk -l
- [ ] mkfs.xfs
- [ ] df -l
- [ ] umount -a

What fdisk option coressponds to primary partition?
- [x] p
- [ ] n
- [ ] P
- [ ] +primary

How you can enable automount?
- [x] add partition to fstab file
- [ ] use `mount -a` 
- [ ] use `umount -a`
- [ ] use `fdisk -s`

## module 11. Working with LVM
Could volume group be extended by logical volume?
- [ ] Yes
- [x] No

How to display all physical volumes?
- [ ] vgdsiplay
- [x] pvdisplay
- [ ] pvcreate -t
- [ ] lvextend

How to extend logical volume by 20% of another lv?
- [x] lvextend -l +20%FREE
- [ ] lvextend -l +20%
- [ ] lvextend -s +20%
- [ ] lvextend -s +20Gb

How to expand physical volume to take all available space?
- [ ] pvextend -l +100%FREE
- [ ] pvdisplay
- [x] pvresize
- [ ] vgextend [pv-name]

## module 12. Processes Hierarchy

How to find multithreaded processes?
- [ ] ps -ejH
- [x] ps -m
- [ ] ps -aux
- [ ] ps --multithreaded

How to list all processes in a tree structure?
- [x] use `ps` with `H` option
- [ ] use `ps` with `t` option
- [ ] use `ps` with `j` option
 
Which signal will kill process?
- [x] `-9`
- [x] `KILL`
- [x] `SIGKILL`

How to kill process by it's name?
- [x] kilall [name]
- [ ] kill -9 [name]
- [ ] kill -15 [name]
- [ ] kill -9 %[name]

How to find job id of the process?
- [ ] ps -aux | grep [name]
- [x] jobs | grep [name]
- [ ] jobs -l
 
Which of these are correct ways to bring process to the background?
- [x] process & 
- [x] bg [process-id]
- [x] bg %[process-id] 
- [ ] process !

Which of the columns reffer to the PID of the process? To the parent's PID?
```bash
[alex@somewhere]~$ ps -ef
root         1     0  2 10:57 ?        00:00:00 /init
root         6     1  0 10:57 tty1     00:00:00 /init
alex         7     6  2 10:57 tty1     00:00:00 -bash 
alex        27     7  0 10:58 tty1     00:00:00 ps -ef
```
- [ ] Third is PID,  second is PPID
- [ ] Fourth is PID, third is PPID
- [x] Second is PID, third is PPID
- [ ] Third is PPID, fourth is PPID

## module 13. SWAP, Memory Usage
What are `uptime`'s load averages time values?
- [ ] 1, 5, 10 mins
- [ ] 1, 10, 20 hours
- [x] 1, 5, 15 mins
- [ ] 1, 10, 20 mins

Which file contains info about cpu?
- [x] /proc/cpuinfo
- [ ] /proc/cpu
- [ ] /etc/cpu
- [ ] /etc/sysinfo

What is the purpose of swap?
- [x] Increase the amount of virtual memory available to a host
- [ ] Increase the amount of disk space on the host
- [ ] Increase performance of the host during high load periods.

How to check, whether your system has configured swap?
- [ ] top
- [x] swapon -s
- [ ] mkswap
- [ ] free -t
How to add file to swap?
## module 14. Linux Bootloaders
What is the correct sequence of boot process?
- [ ] Kernel stage, BIOS stage, Boot loader stage
- [x] BIOS stage, Boot loader stage, Kernel stage
- [ ] Boot loader stage, BIOS stage, Kernel stage


## module 15. InitV System
How many runlevels exists?
- [x] 7
- [ ] 5
- [ ] 9
- [ ] 6

What runlevel would you choose for a webserver?
- [ ] 5
- [ ] 2
- [x] 3
- [ ] 0

What will happen if you set runlevel, which doesn't exist?
- [ ] Nothing, system will start at previous runlevel
- [ ] Nothing, system will start at runlevel 3
- [ ] System will become absolutely unaccessible
- [x] Nothing but GRUB boot choice will be accessible


## module 16. SystemD
How to explore running services on your PC?
- [ ] service show running
- [x] systemctl | grep running
- [x] systemctl --state running
- [ ] service --all

How to check httpd service state?
- [x] systemctl status httpd.service
- [ ] systemctl --state running
- [ ] httpd.service state
- [ ] systemctl list-dependencies

How to restart tomcat service?
- [ ] tomcat.service restart
- [ ] systemctl enable tomcat.service
- [x] systemctl restart tomcat.service
- [ ] systemctl start tomcat.service

Can you change boot order of definite service?
- [x] yes, using `after` and `before` in Unit section 
- [ ] no, it is defined of system

How to get list dependencies of definite service?
- [ ] systemctl
- [ ] systemctl state dependencies
- [ ] systemctl status dependencies
- [x] systemctl list-dependencies --before network.target

## module 18. Using Journalctl
How to get journal records of httpd service?
- [x] journalctl -u httpd.service
- [ ] cat /var/log/httpd
- [ ] journalctl -xe
- [ ] journalctl -b

How to get boot log from journal?
- [ ] journalctl -u httpd.service
- [ ] cat /var/log/httpd
- [ ] journalctl -xe
- [x] journalctl -b

How to get last 7 records from journal?
- [ ] journalctl
- [x] journalctl -n 7
- [ ] journalctl -xe
- [ ] journalctl -b

## module 19. Working with Cron Jobs
Which cron job will be executing every minute?
- [x] * * * * * root date
- [ ] 1 * * * * root date
- [x] */1 * * * * root date

How to create cron job?
- [x] crontab -e
- [ ] crontab -l
- [x] add file to /etc/cron.d/
- [x] add file to /etc/cron.hourly/

## module 20. Software management
How to install without confirmation?
- [x] sudo yum install -y tomcat
- [ ] sudo yum install -f tomcat
- [ ] sudo yum install tomcat

How to check list of configured repositories.
- [ ] yum list -r
- [x] yum repolist
- [ ] sudo yum install epel
- [ ] yum search repo

How to find all duplicates of tomcat?
- [ ] yum list -r
- [ ] yum search duplicates
- [ ] yum search tomcat
- [x] yum search --showduplicates tomcat

How to install the define version etc. nginx?
- [ ] yum search nginx
- [ ] yum install nginx
- [ ] yum install nginx -v 1.10
- [x] yum install nginx-1.10

how to get list of installed rpm packages?
- [x] rpm -qa
- [ ] yum list
- [ ] rpm -ivh
- [ ] rpm -ivh nginx.rpm

How to install rpm package?
- [ ] rpm -qa
- [ ] yum list
- [ ] rpm -ivh
- [x] rpm -ivh nginx.rpm

## module 21. Network Configuration
How to find out your IP address?
- [x] hostname -I
- [x] ifconfig
- [x] ip a

How to check listening tcp ports?
- [ ] ports --all
- [x] netstat -tlpn
- [ ] ifconfig

How to check firewalld state?
- [x] sudo systemctl status firewalld
- [ ] sudo firewalld state
- [ ] sudo firewalld -h

How to turn the network instaface off?
- [x] ifconfig eth0 down
- [ ] ifconfig eth0 up
- [ ] ip eth0 off
- [ ] ip eth0 on

How to turn the network instaface on?
- [ ] ifconfig eth0 down
- [x] ifconfig eth0 up
- [ ] ip eth0 off
- [ ] ip eth0 on 

## module 22. SSH Overview, SCP
How to correctly connect to other OS via SSH? Select right statement.
- [x] ssh user2@192.168.1.10
- [ ] Get-Connect user2@192.168.1.10
- [ ] ping user2@192.168.1.10
- [ ] scp user2@192.168.1.10

How to correctly copy filefrom one OS to the other using SSH?
- [ ] ssh-copy file1 user2@192.168.1.10:/home/user2
- [ ] cp file1 user2@192.168.1.10:/home/user2
- [ ] ssh-copy user2@192.168.1.10:/home/user2 file1
- [x] scp file1 user2@192.168.1.10:/home/user2

## module 23. Basic Apache Configuration
Which ports does httpd listen by default?
- [x] 80
- [x] 443
- [ ] 8080
- [ ] 22

Which logs does httpd store by default?
- [x] error log
- [ ] boot log
- [x] access log
- [ ] catalina.out

Where are the httpd logs stored?
- [ ] /etc/httpd/conf.d/
- [x] /var/log/httpd
- [ ] /etc/httpd/conf
- [ ] /var/www/html


What technology allows you to have many different sites on the httpd?
- [ ] there isn't such opportunity
- [x] Virtual Hosts
- [ ] Virtual Sites

Does httpd allow to listen the content of directory?
- [x] it does
- [ ] it doesn't


Does httpd allow to restrict access to site with login-password?
- [x] it does
- [ ] it doesn't



Where will you place the custom config of httpd?
- [x] /etc/httpd/conf.d/
- [ ] /var/log/httpd
- [ ] /etc/httpd/conf
- [ ] /var/www/html


What is the default document root directory of httpd on CentOS?
- [ ] /var/log/httpd
- [ ] /etc/httpd/conf
- [x] /var/www/html


How to check the site state from Terminal?
- [ ] http http://sitename.com
- [x] curl http://sitename.com
- [ ] state http://sitename.com
- [ ] http://sitename.com

