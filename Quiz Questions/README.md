## Prerequizites
1. Install network tools: `sudo yum install -y net-tools traceroute whois`
2. Make sure httpd web server is running
  
## Tasks

- Check all tcp listening ports: `sudo netstat -tlpn`  
  Which port belongs to httpd web server?
  
- let's change httpd port:
  - in `/etc/httpd/conf/httpd.conf` change line: from `Listen 80` to `Listen 8080`
  - restart httpd service
  - check listening ports again. Which port belongs to httpd web server?
  - change the listening port back to the **80** and check it
  
- check firewall service status  
  check iptables rules: `sudo iptables -L -v -n`
  
- ifconfig tool  
  - display the network interfaces state: `ifconfig -a`.  
    Explore the interfaces. Remember IP address **enp0s8** insterface (etc. 10.6.211.12)
  - switch to the Host OS and run cmd.exe (or terminal if you have LinuxOS)
  - try to ping VM from HostOS: `ping 10.6.211.12`
  - switch to the VM and turn off **enp0s8** interface: `sudo ifconfig enp0s8 down`
  - switch to the Host OS and try to ping VM from HostOS again. What you see?
  - turn on **enp0s8** interface and try to ping VM again
  
- try to ping localhost, 127.0.0.1, 127.0.0.2, 127.0.0.254. Why does it work?
