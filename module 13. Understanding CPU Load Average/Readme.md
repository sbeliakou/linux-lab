## Prerequizites

## Tasks

Run top\htop command, explore options top provides  
 Run top (htop) in background, bring it to foreground, bring back to background, stop process.  
run 2 top and 2 htop processes, find a way to kill only 2 top processes.   
Run the ps -m command and see what processes you have running are multi-threaded.  
Check the load average of your system and see what it's doing.   
Use iostat to view your disk usage.  
Take a look at your running processes, can you see what processes have parents?  
  
  
  
  
Execute swapon -s. Does your system have configured swap?  
Run free -t. What amount of RAM do you have?  
Create swap file by executing fallocate -l 1G /swapfile  
Run ls -lh /swapfile. Does swapfile have correct size?  
Grant 600 permissions to swapfile  
Execute mkswap /swapfile && swapon /swapfile  
Check swapon -s again. What have changed?  
Run free -t. What have changed?  
Run top command, explore options. Who is the biggest RAM consumer?  
Add swapfile to fstab with sed  
Compare free -h results and content of /proc/meminfo file  
Find biggest cpu consumer with top  
Find how many kernels do you have with cat /proc/cpuinfo. Does it differ from info, provided by VirtualBox?  
Move some big file to another place using dd. Check cpu usage with uptime. What have changed after 3 mins? After 15 mins?  
