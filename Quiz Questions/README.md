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

how to archive folder?
- [ ] arch folder1 folder.zip
- [x] tar -czvf myarchive.tar.gz folder1/
- [ ] tar -tvf myarchive.tar.gz
- [ ] tar -xzvf myarchive.tar.gz

how to unarchive folder?
- [ ] arch folder1 folder.zip
- [ ] tar -czvf myarchive.tar.gz folder1/
- [ ] tar -tvf myarchive.tar.gz
- [x] tar -xzvf myarchive.tar.gz

how to explore the content of archive?
- [ ] arch folder1 folder.zip
- [ ] tar -czvf myarchive.tar.gz folder1/
- [x] tar -tvf myarchive.tar.gz
- [ ] tar -xzvf myarchive.tar.gz

How to find myfile file?
- [x] locate myfile
- [x] find / -name "myfile" -type f
- [ ] search myfile
- [ ] where myfile
#### module 07. Linux Users and Groups
How to create group with custom gid?
- [ ] groupadd group_name
- [x] groupadd group_name -g 1250
- [ ] create group 1250

How to create user and assign him to group1?
- [x] useradd -g group1 -G group1 user1
- [ ] useradd user1
- [ ] useradd user1 group1

How to switch to user2?
- [x] su - user2
- [x] su user2
- [ ] su
#### module 08. File Permissions, Links
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

#### module 10. Filesystems, Devices
#### module 11. Working with LVM
#### module 12. Processes Hierarchy
#### module 13. SWAP, Memory Usage
#### module 14. Linux Bootloaders
#### module 15. InitV System
#### module 16. SystemD
#### module 18. Using Journalctl
#### module 19. Working with Cron Jobs
Which cron job will be executing every minute?
- [x] * * * * * root date
- [ ] 1 * * * * root date
- [x] */1 * * * * root date

How to create cron job?
- [x] crontab -e
- [ ] crontab -l
- [x] add file to /etc/cron.d/
- [x] add file to /etc/cron.hourly/
#### module 20. Software management
#### module 21. Network Configuration
#### module 22. SSH Overview, SCP
#### module 23. Basic Apache Configuration
