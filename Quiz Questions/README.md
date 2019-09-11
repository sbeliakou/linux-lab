## Quiz
 
#### module 01. What Linux Is
#### module 02. Linux Family
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

#### module 03. CentOS Installation and Basic Configuration
#### module 04. Basic Shell Usage
How do bash/sh standart prompt look?

How to get to the directory, which is two levels upper?

How to find, in which directory are you now?

How to list content of the directory in reverse order?

How to find info about all command options?

How to clear terminal?

How to find list of all performed commands?

#### module 05. Linux Directories Layout
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

#### module 06. Working with Files
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

#### module 07. Linux Users and Groups
How to create group with custom gid?

How to create user and assign him to group1?

How to switch to user2?

#### module 08. File Permissions, Links
Identify the following permissions: -rwxrw-r--

Select the right octal equivalents for the permissions

How to create symlink to the /home/folder1?

What links are bigger?

Does file movement affect soft link?

#### module 10. Filesystems, Devices
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

#### module 11. Working with LVM
Could volume group be extended by logical volume?

How to display all physical volumes?

How to extend logical volume by 20% of another lv?

How to resize physical volume?

#### module 12. Processes Hierarchy

How to ifnd multithreaded processes?

How to list all processes in a tree structure?

Which signal will kill process?

How to kill process by it's name?

How to find job id of the process?

Which of this are correct ways to bring process to the background?

Which of the columns reffer to the PID of the process? To the parent of the process?
#### module 13. SWAP, Memory Usage
What are `uptime`'s time values?

Which file contains info about cpu?

What is the purpose of swap?

How to check, whether your system has configured swap?

How to add file to swap?
#### module 14. Linux Bootloaders
#### module 15. InitV System
How many runlevels exists?

What runlevel would you choose for a webserver?

What will happen if you set runlevel, which doesn't exist?

How would you bring unexisting runlevel value back to normal?

#### module 16. SystemD
How to explore running services on your PC?

How to check httpd service state?

How to restart tomcat service?

Can you change boot order of definite service?

How to get list dependencies of definite service?

#### module 18. Using Journalctl
How to get journal records of httpd service?

How to get boot log from journal?

How to get last 7 records from journal?

#### module 19. Working with Cron Jobs
Which cron job will be executing every minute?

How to create cron job?

#### module 20. Software management
How to install without confirmation?

How to check list of installed repositories.

How to find duplicates?

How to install the define version etc. nginx?

how to get list of installed rpm packages?

How to install rpm package?

#### module 21. Network Configuration
How to find out your IP address?  

How to check listening tcp ports?  

How to check firewalld state?  

How to turn the network instaface off?  

How to turn the network instaface on? 

#### module 22. SSH Overview, SCP
How to connect to other OS via SSH? Select right statement. 

How to copy filefrom one OS to the other using SSH?  

#### module 23. Basic Apache Configuration
Which ports does httpd listen by default?  

Which logs does httpd store?  

Where are the httpd logs stored?  

What technology allows you to have many different sites on the httpd?  

Does httpd allow to listen the content of directory?  

Does httpd allow to restrict access to site with login-password?  

Where will you place the custom config of httpd?  

What is the default document root directory of httpd?  

How to check the site state from Terminal?  

