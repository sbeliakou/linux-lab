## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

Run systemctl | grep running. What services are currently active?
Run systemctl status httpd. Is it active?
Start httpd service by running systemctl start httpd. Do you have an idea, how to stop it?
Stop httpd
Run systemctl enable httpd, so service will be started every time after reboot. Is this service active now?
Add # before Listen 80 line in /etc/httpd/conf/httpd.conf, then restart httpd
Check status of httpd service. Did something went wrong?
Remove your changes in httpd.conf, then restart the service. What happened?
Open systemd unit file of the httpd service (it is located in /usr/lib/systemd/system)
Change After=network.target to  Before=network.target in the [Unit] section 
Check your changes by running systemctl list-dependencies --before network.target. Is httpd.service listed in there?
Restart the system
Check status of httpd service. What is the problem? How would you fix it?


