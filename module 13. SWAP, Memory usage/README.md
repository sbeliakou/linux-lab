## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

1. Execute `swapon -s`. Does your system have configured swap? 

2. Run `free -t`. What amount of RAM do you have?

3. Create swap file by executing `fallocate -l 1G /swapfile`

4. Run `ls -lh /swapfile`. Does swapfile have correct size? 

5. Grant 600 permissions to swapfile

6. Execute `mkswap /swapfile && swapon /swapfile`

7. Check `swapon -s` again. What have changed? 

8. Run `free -t`. What have changed? 

9. Run `top` command. Who is the biggest RAM consumer?

10. Add swapfile to fstab with `sed`

11. Compare `free -h` results and content of `/proc/meminfo` file

12. Find biggest cpu consumer with `top`

13. Find how many kernels do you have with `cat /proc/cpuinfo`. Does it differ from info, provided by VirtualBox?

14. Move some big file to another place using `dd`. Check cpu usage with `uptime`. What have changed after 3 mins? After 15 mins?  
