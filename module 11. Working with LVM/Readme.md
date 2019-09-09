## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks



Create new physical volume from your disk with pvcreate /dev/[disk-name]
Run vgdisplay. What is the name of your volume group?
Extend your volume group by running vgextend [vg-name] [pv-name]
Run pvscan. What is the size of newly created pv?
Run lvdisplay. What logical volumes are available? Choose one to extend.
Run lvextend -l +100%FREE [lv-name]
Run lvdisplay again. What have changed?
