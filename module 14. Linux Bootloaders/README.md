## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

1. Execute `uname -mrs`. What is the current version of your kernel?

2. Install ELRepo repository:
    * Run `rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org`
    * Add repository with `rpm -Uvh https://www.elrepo.org/elrepo-release-7.0-3.el7.elrepo.noarch.rpm` 

3. Install stable kernel version with `yum --enablerepo=elrepo-kernel install kernel-ml`

4. Reboot your system and choose newly installed kernel

5. Check version of the kernel again. What have changed?
