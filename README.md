## linux-lab

- [x] module 01. What Linux Is
- [x] module 02. Linux Family
- [x] module 03. CentOS Installation and Basic Configuration
- [x] module 04. Basic Shell Usage
- [x] module 05. Linux Directories Layout
- [x] module 06. Working with Files
- [x] module 07. Linux Users and Groups
- [x] module 08. File Permissions, Links
- [x] module 10. Filesystems, Devices
- [x] module 11. Working with LVM
- [x] module 12. Processes Hierarchy
- [x] module 13. SWAP, Memory Usage
- [x] module 14. Linux Bootloaders
- [x] module 15. InitV System
- [x] module 16. SystemD
- [x] module 18. Using Journalctl
- [x] module 19. Working with Cron Jobs
- [x] module 20. Software management
- [x] module 21. Network Configuration
- [x] module 22. SSH Overview, SCP
- [x] module 23. Basic Apache Configuration


## Tools you should get accuineted with:
### Package Management
- [yum](http://man7.org/linux/man-pages/man8/yum.8.html)
- [rpm](https://linux.die.net/man/8/rpm)

### Filesystem, Files and Directories
- [pwd](http://man7.org/linux/man-pages/man1/pwd.1.html) / [cd](http://man7.org/linux/man-pages/man1/cd.1p.html) / [ls](http://man7.org/linux/man-pages/man1/ls.1.html)
- [mkdir](http://man7.org/linux/man-pages/man1/mkdir.1.html) / [rmdir](http://man7.org/linux/man-pages/man1/rmdir.1.html)
- [cp](http://man7.org/linux/man-pages/man1/cp.1.html) / [mv](http://man7.org/linux/man-pages/man1/mv.1.html) / [rm](http://man7.org/linux/man-pages/man1/rm.1.html)
- [touch](http://man7.org/linux/man-pages/man1/touch.1.html)
- [du](http://man7.org/linux/man-pages/man1/du.1.html) / [df](http://man7.org/linux/man-pages/man1/df.1.html)
- [echo](http://man7.org/linux/man-pages/man1/echo.1.html) / [cat](http://man7.org/linux/man-pages/man1/cat.1.html)
- [head](http://man7.org/linux/man-pages/man1/head.1.html) / [tail](http://man7.org/linux/man-pages/man1/tail.1.html)
- [fdisk](http://man7.org/linux/man-pages/man8/fdisk.8.html) / [mkfs](http://man7.org/linux/man-pages/man8/mkfs.8.html)
- [mount](http://man7.org/linux/man-pages/man8/mount.8.html) / [umount](http://man7.org/linux/man-pages/man8/umount.8.html)
- [lsblk](http://man7.org/linux/man-pages/man8/lsblk.8.html) / [partprobe](http://man7.org/linux/man-pages/man8/partprobe.8.html)
- [dd](http://man7.org/linux/man-pages/man1/dd.1.html)
- [tar](http://man7.org/linux/man-pages/man1/tar.1.html) / [zip](https://linux.die.net/man/1/zip) / [unzip](https://linux.die.net/man/1/unzip)
- [locate](http://man7.org/linux/man-pages/man1/locate.1.html) / [find](http://man7.org/linux/man-pages/man1/find.1.html) / [grep](http://man7.org/linux/man-pages/man1/egrep.1.html)
- [ln](http://man7.org/linux/man-pages/man1/ln.1.html) / [unlink](http://man7.org/linux/man-pages/man1/unlink.1.html)

### System Resources, Processes
- [top](http://man7.org/linux/man-pages/man1/top.1.html) / [ps](http://man7.org/linux/man-pages/man1/ps.1.html)
- [uptime](http://man7.org/linux/man-pages/man1/uptime.1.html)
- [free](http://man7.org/linux/man-pages/man1/free.1.html)
- [bg](http://man7.org/linux/man-pages/man1/bg.1p.html) / [fg](http://man7.org/linux/man-pages/man1/fg.1p.html) / [nohup](http://man7.org/linux/man-pages/man1/nohup.1.html)
- [kill](http://man7.org/linux/man-pages/man1/kill.1.html) / [killall](http://man7.org/linux/man-pages/man1/killall.1.html)

### Logical Volumes
- [pvcreate](http://man7.org/linux/man-pages/man8/pvcreate.8.html) / [pvresize](http://man7.org/linux/man-pages/man8/pvresize.8.html) / [pvscan](http://man7.org/linux/man-pages/man8/pvscan.8.html)
- [vgdisplay](http://man7.org/linux/man-pages/man8/vgdisplay.8.html) / [vgextend](http://man7.org/linux/man-pages/man8/vgextend.8.html)
- [lvdisplay](http://man7.org/linux/man-pages/man8/lvdisplay.8.html) / [lvextend](http://man7.org/linux/man-pages/man8/lvextend.8.html)

### File Editors
- [vi/vim](http://man7.org/linux/man-pages/man1/vi.1p.html)

### Manageing Users and Groups
- [id](http://man7.org/linux/man-pages/man1/id.1.html) / [w](http://man7.org/linux/man-pages/man1/w.1.html) / [whoami](http://man7.org/linux/man-pages/man1/whoami.1.html)
- [useradd](http://man7.org/linux/man-pages/man8/useradd.8.html) / [groupadd](http://man7.org/linux/man-pages/man8/groupadd.8.html)
- [usermod](http://man7.org/linux/man-pages/man8/usermod.8.html) / [groupmod](http://man7.org/linux/man-pages/man8/groupmod.8.html)
- [getent](http://man7.org/linux/man-pages/man1/getent.1.html)

### Escalating Privileges
- [su](http://man7.org/linux/man-pages/man1/su.1.html) / [sudo](https://linux.die.net/man/8/sudo)
- [chmod](http://man7.org/linux/man-pages/man1/chmod.1.html) / [chown](http://man7.org/linux/man-pages/man1/chown.1.html)

### Network, Remote Access
- [curl](http://man7.org/linux/man-pages/man1/curl.1.html)
- [ssh](http://man7.org/linux/man-pages/man1/ssh.1.html) / [scp](http://man7.org/linux/man-pages/man1/scp.1.html)
- [ping](http://man7.org/linux/man-pages/man8/ping.8.html)
- [hostname](http://man7.org/linux/man-pages/man1/hostname.1.html) / [ip](http://man7.org/linux/man-pages/man8/ip.8.html) / [ifconfig](http://man7.org/linux/man-pages/man8/ifconfig.8.html)
- [netstat](http://man7.org/linux/man-pages/man8/netstat.8.html)

### System Services
- [systemctl](http://man7.org/linux/man-pages/man1/systemctl.1.html)
- [service](https://linux.die.net/man/8/service)
- [chkconfig](https://linux.die.net/man/8/chkconfig)
- [date](http://man7.org/linux/man-pages/man1/date.1.html)
- [uname](http://man7.org/linux/man-pages/man1/uname.1.html)

### Schedule
- [crontab](http://man7.org/linux/man-pages/man5/crontab.5.html)

### Logs
- [journalctl](http://man7.org/linux/man-pages/man1/journalctl.1.html)
