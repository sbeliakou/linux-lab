## Prerequizites
1. Login to VM as **devops** user  
2. Make sure net-tools are installed
  
## Tasks
#### 1. Installation httpd
- using yum pachage management install httpd
- start httpd service and check the running with netstat and systemctl
- examine access and error logs
  ```bash
  sudo cat /var/log/httpd/access_log 
  sudo cat /var/log/httpd/error_log
  ```
- make a few http requests:
  - using browser: enter `http://localhost` page
  - using **curl** tool: in Terminal execute `curl http://localhost`
- examine access and error logs again. Has something changed?  
  
  
#### 2. Changing document root httpd
- Setting custom page
  - let's turn off default welcome-page  
    `sudo mv /etc/httpd/conf.d/welcome.conf /etc/httpd/conf.d/welcome.conf_backup` 
  - in user home directory create **web-content** folder with index.html file and other content
    ```bash
    cd
    mkdir web-content
    echo "index.html in web-content" > web-content/index.html
    echo "file1 in web-content" > web-content/file1
    echo "file2 in web-content" > web-content/file2
    ```
  - copy created folder to the `/var/www/` directory  
    `sudo cp -r web-content/ /var/www/`
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
  - rename (or delete) index.html file:  
    `sudo mv /var/www/web-content/index.html /var/www/web-content/index.html_backup`
  - restart httpd service
  - make a http requests to `http://localhost` via browser. Describe what you get.  
  
  
#### 3. Basic authentication in httpd
- create file which will contain our credentials:  
  `sudo htpasswd -c /var/www/.htpasswd devops`
- modify `Directory /var/www` section:
  ```bash
  <Directory "/var/www">
      AllowOverride None
      Options +Indexes

      AuthType basic
      AuthName "Private page"
      AuthUserFile "/var/www/.htpasswd"
      Require valid-user
  </Directory>
  ```
- restart httpd service
- make a http requests to `http://localhost` via browser. Describe what you see.
  
  
#### 4. Virtual hosts
- turn on default welcome-page  
  `sudo mv /etc/httpd/conf.d/welcome.conf_backup /etc/httpd/conf.d/welcome.conf`  
- let's create custom content of our new virtual host
  - in user home directory create **simplesite** folder with index.html file and other content
    ```bash
    cd
    mkdir simplesite
    echo "Welcome to the default page of the simplesite" > simplesite/index.html
    ```
  - copy created folder to the `/var/www/` directory  
    `sudo cp -r simplesite/ /var/www/`  
- create config file of new virtualhost and move it to `/etc/httpd/conf.d` directory
  ```bash
  cat << EOF > simplesite.conf
  <VirtualHost 127.0.0.1:80>
      DocumentRoot "/var/www/simplesite"
      ServerName simplesite.com
      
      CustomLog /var/log/httpd/simplesite-access.log combined
      ErrorLog /var/log/httpd/simplesite-error.log
  </VirtualHost>
  EOF
  sudo mv simplesite.conf /etc/httpd/conf.d/
  ```  
- add `127.0.0.1 simplesite.com` line to the `/etc/hosts`  
- restart httpd service  
- make a few http requests to `http://localhost` via browser  
- make a few http requests to `http://simplesite.com` via browser  
- explore access and error log of default site and our simplesite.com  
  
Create yourself one more virtual host for training.  
