## Prerequizites
1. Install network tools: `sudo yum install -y net-tools traceroute whois`
2. Make sure httpd web server is running

## Tasks

- let's check internet connection:
  ```bash
  ping epam.com
  sudo traceroute -I epam.com
  ```
  
- Check your IP addresses. try to execute:
  ```bash
  hostname -I
  ifconfig
  ip a
  ```

- Check all tcp listening ports: `sudo netstat -tlpn`
  Which port belongs to httpd web server?
  You can filter out output using **grep**: `sudo netstat -tlpn | grep httpd`
  
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


## Helpful Materials
- https://www.youtube.com/watch?v=S5GwXdXPOdU&list=PLtGnc4I6s8duKXPypO75QPvD4ZsmXpYc2&index=22
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/networking_guide/sec-network_bridging_using_the_networkmanager_command_line_tool_nmcli