## Prerequizites
1. Login to VM as **devops** user
2. Make sure net-tools are installed
  
## Tasks
1. Installation httpd
- using yum pachage management install httpd
- start httpd service and check the running with netstat and systemctl
- examine access and error logs: `sudo cat /var/log/httpd/access_log`, `sudo cat /var/log/httpd/error_log`
- make a few http requests:
  - using browser: enter `http://localhost` page
  - using **curl** tool: in Terminal execute `curl http://localhost`
- examine access and error logs again. Has something changed?  
  
  
2. Changing document root httpd
- Setting custom page
  - let's turn off default welcome-page: `sudo mv /etc/httpd/conf.d/welcome.conf /etc/httpd/conf.d/welcome.conf_backup` 
  - in user home directory create **web-content** folder with index.html file and other content
  ```bash
  cd
  mkdir web-content
  echo "index.html in web-content" > web-content/index.html
  echo "file1 in web-content" > web-content/file1
  echo "file2 in web-content" > web-content/file2
  ```
  - copy created folder to the `/var/www/` directory: `sudo cp -r web-content/ /var/www/`
  - using sed in `/etc/httpd/conf/httpd.conf` file change DocumentRoot from `"/var/www/html"` to `"/var/www/web-content"`
  - restart httpd service
  - make a few http requests to `http://localhost` via browser and **curl** tool. Describe what you get.  
  
- Viewing files in directory
  - add option file listening - in httpd config file add `Options +Indexes` line to the `Directory /var/www` section:
  ```bash
  <Directory "/var/www">
      Options +Indexes
      ...
  </Directory>
  ```
  - rename (or delete) index.html file: `sudo mv /var/www/web-content/index.html /var/www/web-content/index.html_backup`
  - restart httpd service
  - make a http requests to `http://localhost` via browser. Describe what you get.  

3
httpd + basic auth

4
Virtual hosts
