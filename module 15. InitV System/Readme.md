
## Quiz

1. How many runlevels exists?
2. What runlevel would you choose for a server?
3. What will happen if you set runlevel, which doesn't exist?
4. How would you bring unexisting runlevel value back to normal?
  
## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)
2. Install Apache by running `yum update` and then `yum install -y httpd`
  
## Tasks

1. Start httpd by using `service httpd start`

2. Check it's status with `service httpd status`

3. Check what services are currently active with `service --status-all`

4. Make httpd start at boot time with `chkconfig httpd on`

5. Reboot and check status of httpd. Did it start automatically?

5. Stop service

6. Disable httpd from starting at a boot time

