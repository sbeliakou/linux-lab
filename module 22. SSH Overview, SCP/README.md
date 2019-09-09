## Prerequizites
1. Log in to VM as **devops** user and find out IP address of brigde interface (**enp0s8**)  
![](images/1_get_vm_ip.PNG)
2. Make sure sshd service is enabled
  
## Tasks

1. SSH connection
  - For Windows as Host OS  
    - download and install SSH client (etc. [PuTTY](https://www.putty.org/))  
    - run PuTTY. In Configuration window enter early remembered IP-address (etc. 10.6.211.12) in "Host Name (or IP address)" field  
    ![](images/2_enter_ip.PNG)  

    - in appeared message select "yes" for approving ssh keys exchange  
    ![](images/3_accept_key.PNG)  

    - enter as **devops** user  
    ![](images/4_log_in.PNG)  

    - now you are in VM os. try execute "hostname", "uname -a"  
    ![](images/5_result.PNG)  


  - For Linux as Host OS
    - run Terminal
    - establish ssh connection by executing: `ssh devops@10.6.211.12`  
    ![](images/6_ssh_linux2linux.PNG)  
  
2. Copying files by SSH
  - For Windows as Host OS  
    - download and install SCP client (etc. [PSCP](https://the.earth.li/~sgtatham/putty/latest/w64/pscp.exe))  
    - open PowerShell and execute `pscp -V` to check installation  
    ![](images/7_pscp_check_v.PNG)  
    - get files list in **devops** home directory: `pscp -ls devops@10.6.211.12:/home/devops`  
    ![](images/8_pscp_ls.PNG)  
    - copy file to VM: `pscp .\test_scp_file.txt devops@10.6.211.12:/home/devops/Desktop`  
    ![](images/9_pscp_copy.PNG)  
    - check the copying  
    ![](images/10_pscp_check.PNG)  


  - For Linux as Host OS
    - run Terminal
    - let's create test file and copy it to **devops** user on VM  
    ![](images/11_scp_linux2linux.PNG)  
    - check the copying  
    ![](images/12_scp_check.PNG)  




