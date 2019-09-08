## Prerequizites
1. Make sure Virtualization Technology is enabled in BIOS.
2. Download and install VirtualBox. (https://www.virtualbox.org/wiki/Downloads)
3. Download CentOS 7 DVD ISO image. (https://www.centos.org/download/)
4. Make sure hypervisor launch type is disabled. (https://stackoverflow.com/a/50119065)

## Tasks

### 1. Creating a new virtual machine
Run VirtualBox and create a new virtual machine with the following requirements:
- Name: centos7 (etc.)
- Memory size: >= 1024 Mb
- Hard disk: create a dynamically allocated VDI virtual hard disk with size >= 10Gb
- In settings of created VM enable 2nd network adapter attached to Bridged Adapter
- In settings of created VM choose Storage section -> Controller IDE -> Empty and in Attributes subsection click on the disk icon and choose CentOS ISO image

### 2. Installing CentOS
Run created VM and choose Install CentOS.
Intstalling parameters:
- Language - English
- Software Selection - Gnome Desktop or KDE plasma Workspaces (up to you)
- Installation Destination - apply default settings
- Network and Hostname - Ethernet-Configure-General-Mark "Automatically connect to this network ..." (repeate for 2nd adapter)

- Set root password
- Create user "devops". Don't make this user administrator. Leave the remaining settings unchanged

### 3. Running CentOS
Log in to installed CentOS with "devops" credentials.
Explore CentOS graphical interface, find files viewer, terminal emulator, simple text editor.
