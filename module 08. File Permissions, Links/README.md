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
  
11. Switching to other users, permissions
  - execute `id` and look to user and group information for the current user
  - tasks with **user1**:
    - switch to the **user1**: `su - user1`
    - get, examine and describe user and group information for the current user
    - create file **/tmp/user1_test** with some content
    - set permissions with `chmod 600 user1_test`
    - examine permissions of **/tmp/user1_test** with `ls -l`. Describe what you see.
    - copy **/tmp/user1_test** to /opt directory
    - log out from **user1** by executing `exit`
  - tasks with **user1200**:
    - log in as **user1200** user by executing `su user1200`
    - get, examine and describe user and group information for the current user
    - try to read the **/tmp/user1_test file** content, try delete the file. Describe what you see?
    - log out from **user1200**
  - tasks with **root**
    - log in as root
    - try to read the **/opt/user1_test**, then try to delete it. Describe what you see
    - create directory **/opt/root_dir**, copy file **user1_test** there. What permissions does copied file have? What
      permissions does directory have?
    - log out from **root** and log in as **user1**. Can you delete **/opt/root_dir/user1_test**? Why?
  - describe the difference between `su ...` and `su - ...` command
  - What permissions does user's home directory have?
  
12. Executable permissions
  - tasks with **user1**:
    - create file **~/user1_test** with content:
      ```bash
      #!/bin/bash
      echo "Hello from user1_test"
      ```
    - examine permissions of **~/user1_test**. Describe what you see.
    - try runinnig `./user1_test`. What happened? Why?
    - set executable permissions with `chmod u+x user1_test`. Can you run file now?
    - create new directory **user1_dir**
    - examine permissions of **~/user1_dir**. Describe what you see.
    - set permissions to **user1_dir**, so there is no `x`. Can you access this directory? Can you rename it? 
    
13. Create symlink with `ln -s /etc/filesystems mylink1`. What size does it have?

14. Create symlink with `ln /etc/filesystems mylink2`. What size does it have?

15. Rename `/etc/filesystems` to `/etc/fs`

16. Check content of mylink1 and mylink2

17. Rename `/etc/fs` back
