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
    - what is the difference between `/etc/passwd` and `getent`?

4. Delegate root privelegies
  - login as **devops** user. try to explore of **/etc/sudoers** file. What's happened? Let's give permissions to **devops** user.
  - login as root-user
  - create new file in `/etc/sudoers.d` directory: `visudo -f /etc/sudoers.d/devops`
  - enter to the new file the following lines: `devops ALL=(ALL) NOPASSWD: ALL`
  - go back to **devops** user
  - try to explore of **/etc/sudoers** file again.  Did you get the access?
  - try to execute `sudo cat /etc/sudoers`. What's happened?


## Helpful Materials
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/s2-users-cl-tools
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/s2-groups-cl-tools
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/chap-deployment_guide-gaining_privileges
- https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/sect-deployment_guide-gaining_privileges-the_sudo_command
