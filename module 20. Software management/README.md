## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

### 1. YUM package management
- Tomcat installation
  - install Tomcat application server: `sudo yum install tomcat tomcat-webapps`
  - inspect which packets were installed, where were they installed from
  - run tomcat service: `sudo systemctl start tomcat.service`
  - now enter in your browser http://localhost:8080 and you'll tomcat home page.

- repository installation
  - check list of installed repositories
  - install EPEL (epel-release) repository
  - check list of installed repositories again. Are there a new entries?

- Nginx installation
  - install Nginx web server without install confirmation
  - now you can run nginx.service and see homepage http://localhost

- uninstalling
  - stop both services (tomcat and nginx) and remove them with one line and without confirmation

- package searching
  - look for which package contains ifconfig tool.

- update your system

- show duplicates of tomcat web server

- install the earliest version of tomcat (etc. tomcat-7.0.76-7.el7_5)

### 2. RPM package management
- check of installed packages via `rpm -qa`. Count them and remember their quantity.
- [download rpm package](https://archive.apache.org/dist/httpd/binaries/rpm/x86_64/httpd-2.2.2-1.x86_64.rpm) of httpd web server, install it via `rpm -ivh` and run httpd service
- check count of installed packages again and compare with previous number. How many packages were installed?
- look for the paths of all httpd files


## Helpful Materials
- https://www.youtube.com/watch?v=WU-MoPJsK9U&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=45
- https://www.youtube.com/watch?v=kQ59WV9lJU8&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=46
- https://www.youtube.com/watch?v=O2kKklCnD9Q&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=47
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/sec-working_with_packages
