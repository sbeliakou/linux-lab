## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)
  
## Tasks

1. Getting current user information
  - execute `id` and look to user and group information for the current user
  - describe which groups user belongs to? What are their gid?
  
2. Group creating
    - login as root-user: execute `su` and enter root-password
    - create group **group1**: `groupadd group1`
    - create group **group1200** with gid=1200: `groupadd group1200 -g 1200`
    - examine of created groups: `cat /etc/group | grep group*`. Describe what you see.
    - try to create new group with name **group1**. Describe what you see.
  
3. User creating
    - let's create user **user1** and assign him to **group1**: `useradd -g group1 -G group1 user1`
    - set the password for **user1**: `passwd user1`
    - create user **user1200** with uid=1200 and assign him to **group1200** as initial login group and to **group1200**, **group1** as supplementary groups
    - set the password for **user1200**
    - examine of created users:
      - `id user1`, `id user1200`
      - `cat /etc/group | grep ^group*`
      - `cat /etc/passwd | grep ^user1*`
      - `getent passwd | grep ^user1200*`
      - `getent passwd | grep ^group1200*`
  
4. Switching to other users, permissions
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
  
4.1 Executable permissions
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
    
5. Delegate root privelegies
  - login as **devops** user. try to explore of **/etc/sudoers** file. What's happened? Let's give permissions to **devops** user.
  - login as root-user
  - create new file in `/etc/sudoers.d` directory: `visudo -f /etc/sudoers.d/devops`
  - enter to the new file the following lines: `devops ALL=(ALL) NOPASSWD: ALL`
  - go back to **devops** user
  - try to explore of **/etc/sudoers** file again.  Did you get the access?
  - try to execute `sudo cat /etc/sudoers`. What's happened?
