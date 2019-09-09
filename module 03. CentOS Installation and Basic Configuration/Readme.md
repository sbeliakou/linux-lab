## Prerequizites
1. Make sure Virtualization Technology is enabled in BIOS.
2. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
3. Download [CentOS DVD ISO image](https://www.centos.org/download/).
4. Make sure hypervisor launch type is disabled. [Link](https://stackoverflow.com/a/50119065)

## Tasks

### 1. Creating a new virtual machine
Run VirtualBox and create a new virtual machine with the following requirements:
- Name: centos7 (etc.)  
![](images/2_vb_name_os.png "")  
  
- Memory size: >= 1024 Mb  
![](images/3_vb_memory_size.png "")  
  
- Hard disk: create a dynamically allocated VDI virtual hard disk with size >= 10Gb  
![](images/4_vb_new_hard_disk.png "")  
![](images/5_vb_hard_disk_file_type.png "")  
![](images/6_vb_storage_on_hd.png "")  
![](images/7_vb_file_location_size.png "")  
  
- In settings of created VM enable 2nd network adapter attached to Bridged Adapter  
![](images/8_vb_settings_vm.png "")  
![](images/9_vb_1st_network_adapter.PNG "")  
![](images/10_vb_2nd_network_adapter.PNG "")  
  
- In settings of created VM choose CentOS ISO image  
![](images/10_vb_choose_disk_image.png "")  
![](images/11_vb_choose_disk_image_2.png "")  
  
  
### 2. Installing CentOS
- start virtual machine  
![](images/12_vb_start_vm.png "")  
  
- choose install CentOS 7  
![](images/13_cs7_install.png "")  
![](images/14_cs7_install.png "")  
  
- set language  
![](images/15_cs7_install_lang.png "")  
  
- set timezone  
![](images/16_cs7_install_timezone.png "")  
![](images/17_cs7_install_timezone_2.png "")  
  
- set hard disk partition layout - leave default 
![](images/18_cs7_install_layout.png "")  
  
- choose software  
![](images/19_cs7_install_software_1.png "")  
![](images/19_cs7_install_software_2.png "")  
![](images/20_cs7_install_main.png "")  
  
- Set root password  
![](images/21_cs7_install_root.png "")  
![](images/22_cs7_install_root_pwd.png "")  
  
- Create user "devops". Don't make this user administrator. Leave the remaining settings unchanged  
![](images/23_cs7_install_user.png "")  
![](images/24_cs7_install_user_pwd.png "")  
  
- apply licence  
![](images/28_cs7_install_lic.png "")  
  
- Network and Hostname - Ethernet-Configure-General-Mark "Automatically connect to this network ..." (repeate for 2nd adapter)  
![](images/29_cs7_install_init_net.png "")  
![](images/30_cs7_install_network.PNG "")  
![](images/31_cs7_install_network.PNG "")  
![](images/32_cs7_install_network.PNG "")  
![](images/33_cs7_install_network.PNG "")  
![](images/34_cs7_install_network.PNG "")  
![](images/35_cs7_install_network.PNG "")  
  
### 3. Running CentOS
- log in to installed CentOS with "devops" credentials.  
![](images/36_cs7_install_login.png "")  
![](images/37_cs7_install_login.png "")  
  
- explore CentOS graphical interface, find files viewer, terminal emulator, simple text editor.  
![](images/38_cs7_install_ready.png "")  
  
