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
    
 4. Switching to other users, permissions
  - execute `id` and look to user and group information for the current user
  - tasks with **user1**:
    - switch to the **user1**: `su - user1`
    - get, examine and describe user and group information for the current user
    - create file **/tmp/user1_test** with the some content
    - set permissions to **rw-------**
    - examine permissions of **/tmp/user1_test**. Describe what you see.
    - log out from **user1** by executing `exit`
  - tasks with **user1200**:
    - log in as **user1200** user by executing `su user1200`
    - get, examine and describe user and group information for the current user
    - try to read the **/tmp/user1_test file** content, try delete the file. Describe what you see?
    - log out from **user1200**
  - describe the difference between `su ...` and `su - ...` command
