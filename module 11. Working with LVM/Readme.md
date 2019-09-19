## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)
2. List your partitions from Task 10. What size does it have?

## Tasks

1. Create new physical volume from your partition with `pvcreate /dev/[disk-name][part-number]`

2. Run `pvresize /dev/[disk-name][part-number]` to utilize all space on disk

3. Run `pvscan`. What is the size of newly created pv?

4. Run `vgdisplay`. What is the name of your volume group?

5. Extend your volume group by running `vgextend [vg-name] [pv-name]`. What is the size now?

6. Run `lvdisplay`. What logical volumes are available? Choose one to extend.

7. Run `lvextend -l +100%FREE [lv-name]`

8. Run `lvdisplay` again. What have changed?


## Helpful Materials
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/logical_volume_manager_administration/logical_volumes
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/logical_volume_manager_administration/lvm_cli
- https://codingbee.net/rhcsa/rhcsa-logical-volume-management-lvm-overview
- https://www.thegeekdiary.com/redhat-centos-a-beginners-guide-to-lvm-logical-volume-manager/
