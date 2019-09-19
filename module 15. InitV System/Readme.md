
## Quiz

1. How many runlevels exists?
2. What runlevel would you choose for a server?
3. What will happen if you set runlevel, which doesn't exist?
4. How would you bring unexisting runlevel value back to normal?

## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)
2. Install Apache by running `sudo yum update` and then `sudo yum install -y httpd`

## Tasks

1. Start httpd by using `sudo service httpd start`

2. Check it's status with `sudo service httpd status`

3. Check what services are currently active with `sudo service --status-all`

4. Make httpd start at boot time with `sudo chkconfig httpd on`

5. Reboot and check status of httpd. Did it start automatically?

5. Stop service

6. Disable httpd from starting at a boot time


## Helpful Materials
- https://www.youtube.com/watch?v=5JVvLdutDlg&list=PLtGnc4I6s8duKXPypO75QPvD4ZsmXpYc2&index=27
