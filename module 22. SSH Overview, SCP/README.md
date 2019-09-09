## Prerequizites
1. Log in to VM as **devops** user and find out IP address of brigde interface (**enp0s8**)  
![](images/1_get_vm_ip.PNG)
2. Make sure sshd service is enabled
  
## Tasks

1. For Windows OS as Host OS  
- download and install SSH client (etc. [PuTTY](https://www.putty.org/))  
- run PuTTY. In Configurqation window enter early remembered IP-address (etc. 10.6.211.12) in "Host Name (or IP address)" field  
![](images/2_enter_ip.PNG)  
  
- in appeared message select "yes" for approving ssh keys exchange  
![](images/3_accept_key.PNG)  
  
- enter username "devops" and password  
![](images/4_log_in.PNG)  
  
- now you are in VM os. try execute "hostname", "uname -a"  
![](images/5_result.PNG)  
  

2. For Linux OS as Host OS

