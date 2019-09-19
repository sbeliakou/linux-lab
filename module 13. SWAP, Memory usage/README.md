## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

### 1. Swap configuration

- Execute `swapon -s`. Does your system have configured swap?

- Run `free -t`. What amount of RAM do you have?

- Create swap file by executing `fallocate -l 1G /swapfile`

- Run `ls -lh /swapfile`. Does swapfile have correct size?

- Grant 600 permissions to swapfile

- Execute `mkswap /swapfile && swapon /swapfile`

- Check `swapon -s` again. What have changed?

- Add swapfile to fstab with `sed`

### 2. Gathering memory info 

- Run `free -t`. What have changed?

- Run `top` command. Who is the biggest RAM consumer?

- Compare `free -h` results and content of `/proc/meminfo` file

- Find biggest cpu consumer with `top`

### 3. Gathering cpu info

- Find how many kernels do you have with `cat /proc/cpuinfo`. Does it differ from info, provided by VirtualBox?

- Move some big file to another place using `dd`. Check cpu usage with `uptime`. What have changed after 3 mins? After 15 mins?


## Helpful Materials
- https://www.youtube.com/watch?v=D25qsn00mJQ&list=PLtGnc4I6s8duKXPypO75QPvD4ZsmXpYc2&index=23
- https://www.youtube.com/watch?v=0kon1nHz3Hk&list=PLtGnc4I6s8duKXPypO75QPvD4ZsmXpYc2&index=1
- https://www.youtube.com/watch?v=awtr9QEmXHE&list=PLtGnc4I6s8duKXPypO75QPvD4ZsmXpYc2&index=2
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/s1-sysinfo-memory-usage
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/s1-sysinfo-cpu
