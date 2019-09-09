## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

1. Execute `cd ~`. Check in which directory we are?

2. Folder creating
  - create folder **task6**: `mkdir task6`
  - explore the content of current directory and make sure **task6** was created
  - enter to the **task6** folder. 
  
3. File creating: touch-way
  - create **test1** file: `touch test1`
  - explore the content of current directory, make sure **test1** was created. How big is it?
  
4. File creating: with **vi**
  - run `vi test2`
  - you are in Vi text editor now: 
    - press `i` to enter in insert mode
    - input `Hello file`
    - press `Esc` to get in normal mode
    - enter `:wq` to save and exit
  - let's see the content of **test2** file: `cat test2`. What can you see?
  - explore the content of current directory, how many files are there now?
  
5. File creating: redirection-way
  - execute `echo 'Hello, another file' > test3`
  - explore the content of current directory again. What can you see? Get the content of created file.
  - execute `echo 'Hello batman' > test3` and explore the content of **test3** file again. What you see?
  - execute `echo 'Hello joker' >> test3` and explore the content of **test3** file again. Describe what you see?
  
6. File creating: with **cat**
  - let's create multiline file:
    ```bash
    cat << 'EOF' > test4
    line1
    line2
    line3
    line4
    EOF
    ```
  - let's see the first 2 lines in created file: `head -n 2 test4`
  - let's see the last 3 lines in created file: `tail -n 3 test4`
  - create text file with at least 15 text lines and examine `head` and `tail` command with different options and without them.
  
7. Copy, move, rename
  - create folder **task6_sub**
  - let's make a copy of **test2** file: `cp test2 test2_copy`. Explore the content of current directory, how many files are there now?
  - let's move a copied file into new folder: `mv test2_copy task6_sub/`
  - explore the content of current and **task6_sub** directory: `ls -l`, `ls -l task6_sub/`
  - rename **task6_sub/test2_copy** file: `mv task6_sub/test2_copy task6_sub/test2_new_name`. check the renaming.
  - rename **task6_sub** folder. check the renaming.
  
8. Executed files
  - go to the **task6** folder and print the **test2** file content.
  - let's rewrite the file: `echo 'echo $PATH' > test2`. Print the **test2** file content again.
  - edit **test2** with **vi** - add `#!/bin/bash` as the first line of the file.
  - get list-view of the **test2** file: `ls -l test2`
  - execute `chmod +x test2`
  - get list-view of the **test2** file again. What have changed?
  - now we can run **test2** by executing `./test2`. What has happend?
  
9. Archiving
  - go to the home directory. Explore the content of current directory and make sure there is **task6** folder here.
  - let's archive this folder: `tar -czvf test.tar.gz`. 
  - explore the content of current directory and make sure there is **test.tar.gz** archive here.
  - Unarchive **test.tar.gz** to the temp directory.

10. Files searching
  - go to the home directory. Explore the content of current directory and make sure there is **task6** folder here.
  - try to find **passwd** file: `locate passwd`
  - let's find all task* directories in home directory: `find $HOME -name "task*" -type d`
  - let's find all test* files in home directory: `find $HOME -name "test*" -type f`
  - let's find all executed test* files in home directory: `find $HOME -name "test*" -type f -perm /a+x`
  - explore the opportunities of find command (`man find`) and find all files in home directory not older than 3 hours
  
  
