## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

1. Execute `uname -mrs`. What is the current version of your kernel?

2. Install ELRepo repository:
    * Run `sudo rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org`
    * Add repository with `sudo rpm -Uvh https://www.elrepo.org/elrepo-release-7.0-3.el7.elrepo.noarch.rpm`

3. Install stable kernel version with `sudo yum --enablerepo=elrepo-kernel install kernel-ml`

4. Reboot your system and choose newly installed kernel

5. Check version of the kernel again. What have changed?


## Helpful Materials
- https://www.golinuxcloud.com/linux-boot-process-explained-step-detail/
- https://www.youtube.com/watch?v=lxJI8Pmf1e4&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=17
- https://www.youtube.com/watch?v=j5ppVpr-qSA&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=18
- https://www.youtube.com/watch?v=RnviHf763Q4&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=19
- https://katacoda.com/cybershaolin/courses/intro-to-linux/linux-os
