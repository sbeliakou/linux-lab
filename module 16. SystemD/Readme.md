## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)
2. Install Apache by running `yum update` and then `yum install -y httpd`

## Tasks

### 1. Basic systemd commands

- Run `systemctl | grep running` or `systemctl --state running`. What services are currently active?

- Run `systemctl status httpd`. Is it active?

- Start httpd service by running `systemctl start httpd`. Do you have an idea, how to stop it?

- Stop httpd

- Run `systemctl enable httpd`, so service will be started every time after reboot. Is this service active now?

### 2. Starting broken service

- Add # before Listen 80 line in `/etc/httpd/conf/httpd.conf`, then restart httpd

- Check status of httpd service. Did something went wrong?

- Remove your changes from `httpd.conf`, then restart the service. What happened?

### 3. Working with service files

- Open systemd unit file of the httpd service (it is located in `/usr/lib/systemd/system`)

- Change `After=network.target` to  `Before=network.target` in the [Unit] section

- Check your changes by running `systemctl list-dependencies --before network.target`. Is httpd.service listed in there?

- Restart the system

- Check status of httpd service. What is the problem? How would you fix it?

- Remove your changes from `/usr/lib/systemd/system`, then restart the service.

- Check default page in browser at http://127.0.0.1:80

### 4. Rebooting system

- Moreover, **systemctl** may be used to manage system: 
  - explore **System Commands** section in `systemctl --help`
  - reboot your server using `systemctl`  
  (note: apart from that you can use `shutdown -r now`)


## Helpful Materials
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/sect-managing_services_with_systemd-services
- https://www.golinuxcloud.com/beginners-guide-systemd-tutorial-linux/
