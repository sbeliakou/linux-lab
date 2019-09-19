## Prerequizites

1. Log in to VM as **devops** user and run Terminal (Applications - System Tools - Terminal)
2. Go to the **devops** home directory

## Tasks

#### 1. Getting permissions info
- using command `ls -l` get the directory content as list
- examine 1st, 3rd and 4th columns. Describe their meaning. What do **d**, **r**, **w**, **x**, **.** symbols mean?
- exercise in permissions transformation:
  - transform from decimal to literal:
    - 777; 766; 754; 644; 400; 600
  - tranform from literal to decimal:
    - -rwxrwxrwx.
    - -rw--w-r--.
    - -rw-rwxrw-.
    - -r-------x.
    - -rwxr-xr-x.


#### 2. Permissions
Create **permissions_task** directory and go into it.
Create 7 files with names file1, ..., file7.

##### 1. chmod usage
- decimal numbers
  - let's set all permissions for all users for **file1** file: `chmod 777 file1`
  - let's remove all permissions for all users for **file2** file: `chmod 000 file2`
  - set the following permissions using `chmod` with decimal numbers

    | File name | User perm-s | Group perm-s | Others perm-s |
    | --------- | ----------- | ------------ | ------------- |
    | file3  | read, execute | write, execute | read, write |
    | file4  | read, write | read, execute | read |
    | file5  | write, execute | read, write, execute | read, execute |
    | file6  | read, write, execute | read,  execute | read, write |
    | file7  | read | read, write | write, execute |
  - check all permissions were given correctly

- using letters
  - let's check **file1** permissions: `-rwxrwxrwx. 1 devops devops 0 Sep 11 10:41 file1`
  - let's delete user's read-permission for **file1** file: `chmod u-r file1`
  - let's delete group's write-permission for **file1** file: `chmod g-w file1`
  - let's delete other's execute-permission for **file1** file: `chmod o-x file1`
  - in result you shuld get the following result: `--wxr-xrw-. 1 devops devops 0 Sep 11 10:41 file1`

  - let's check **file2** permissions: `----------. 1 devops devops 0 Sep 11 10:41 file2`
  - let's add read-permission for all: `chmod a+r file2`
  - let's add write-permission for group: `chmod g+w file2`
  - also you can add definite permission for **all**: `chmod a+x file2`
  - as result we've get: `-r-xrwxr-x. 1 devops devops 0 Sep 11 10:41 file2`

  - finally, instead decimal numbers we can write letter permissions for each entity separately:
  ```bash
  [devops@localhost permissions_task]$ ls -l file2
  -r-xrwxr-x.  1  devops  devops  0  Sep 11 10:41  file2
  [devops@localhost permissions_task]$ chmod u=w,g=,o=w file2
  [devops@localhost permissions_task]$ ls -l file2
  --w-----w-.  1  devops  devops  0  Sep 11 10:41  file2
  [devops@localhost permissions_task]$ chmod u=,g=rwx,o=rx file2
  [devops@localhost permissions_task]$ ls -l file2
  ----rwxr-x.  1  devops  devops  0  Sep 11 10:41  file2
  ```

- using letter-way set the following permissions for the files:

  | File name | User perm-s | Group perm-s | Others perm-s |
  | --------- | ----------- | ------------ | ------------- |
  | file1  | write, execute | write | read, write, execute |
  | file2  | read, | read, write, execute | write |
  | file3  | read, write, execute |  write | read, execute |
  | file4  | read,  execute | read, write, execute | read, write |
  | file5  | write, execute | read, write | write, execute |
  | file6  | read, execute |  write, execute | read, |
  | file7  | read, write | read, write | read, write, execute |


##### 2. how permissions work
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


##### 3. Executable permissions
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


#### 4. Ownership
- tasks with **user1**:
  - create new directory **~/user1_storage** with files `file1` and `file2` stored in it 
  - examine directory and files permissions. Describe what you see
  - make **root** owner of `file1` with `chown root: ~/user1_storage/file1`. Can you change this file now?
  - change directory ownership with `chown user1: -R ~/user1_storage`. Can you change `file1` now?
  
#### 5. Symlink, hardlink
- Create symlink with `ln -s /etc/filesystems mylink1`. What size does it have?
- Create symlink with `ln /etc/filesystems mylink2`. What size does it have?

- Removing source file:
  - rename `/etc/filesystems` to `/etc/fs`
  - check content of mylink1 and mylink2. What happened?
  - rename `/etc/fs` back

- Remove links:
  - use `unlink mylink1`. What happened?
  - use `rm mylink2`. How have your working directory changed?
  
- Get origin path from link
  - execute `which java` and explore the provided directory. Where does symlink point?
  - go link after link and find, where the original file is.

## Helpful Materials
- https://www.youtube.com/watch?v=rp3CDGGnFL0&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=30
- https://www.youtube.com/watch?v=_7Hfq6JS7u8&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=31
- https://www.youtube.com/watch?v=K0KrP4tzLg8&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=34
- https://www.youtube.com/watch?v=edjzPpc9oKY&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=53
- https://www.youtube.com/watch?v=f4brdaS2bFs&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=54
- https://www.youtube.com/watch?v=pAhG9H_hIHw&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=55
- https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Step_by_Step_Guide/s1-managing-locating.html
- https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Step_by_Step_Guide/s1-navigating-ownership.html
