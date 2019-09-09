## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

1. Create test-1 and test-2 files in `/tmp` directory

2. Give everyone permissions to do everything with test-1 by `chmod 777 test-1`

3. Give test-2 permissions  rw-------. Can you change this file?

4. Log out and log in as a root. Do you have access to this file now?

5. Exclude executable permissions from test-1. Can you run it now? Can you run it as root?

6. Set user1200 as owner of the test-1 with `chown user1200:group1200 test-1`

7. Create new directory test-dir. Set user1 as it's owner

8. Copy test-2 to test-dir. Does user1 have permissions to read this file?

9. Give test-2 permissions 750

10. Change group permissions on test-dir with `chgrp group1 test-2`. Does user1 have permissions to read this file?

11. Create symlink with `ln -s /etc/filesystems mylink1`. What size does it have?

12. Create symlink with `ln /etc/filesystems mylink2`. What size does it have?

13. Rename `/etc/filesystems` to `/etc/fs`

14. Check content of mylink1 and mylink2

15. Rename `/etc/fs` back


