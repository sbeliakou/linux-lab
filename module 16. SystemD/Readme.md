## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)
2. Install Apache by running `yum update` and then `yum install -y httpd`

## Tasks

1. Run `systemctl | grep running` or `systemctl --state running`. What services are currently active?

2. Run `systemctl status httpd`. Is it active?

3. Start httpd service by running `systemctl start httpd`. Do you have an idea, how to stop it?

4. Stop httpd

5. Run `systemctl enable httpd`, so service will be started every time after reboot. Is this service active now?

6. Add # before Listen 80 line in `/etc/httpd/conf/httpd.conf`, then restart httpd

7. Check status of httpd service. Did something went wrong?

8. Remove your changes from `httpd.conf`, then restart the service. What happened?

9. Open systemd unit file of the httpd service (it is located in `/usr/lib/systemd/system`)

10. Change `After=network.target` to  `Before=network.target` in the [Unit] section

11. Check your changes by running `systemctl list-dependencies --before network.target`. Is httpd.service listed in there?

12. Restart the system

13. Check status of httpd service. What is the problem? How would you fix it?

14. Remove your changes from `/usr/lib/systemd/system`, then restart the service.

15. Check default page in browser at http://127.0.0.1:80


## Helpful Materials
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/sect-managing_services_with_systemd-services
- https://www.golinuxcloud.com/beginners-guide-systemd-tutorial-linux/
