## Prerequizites
1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

Execute `cd ~`. Check in which directory we are?

#### 1. Working with folders
1. Folder creating:
  - create empty folder **folder1**:
    `mkdir folder1`
  - create empty folders **folder2**, **folder3** using one-line command
  - moreover you can create subdirectories at the same time:
    `mkdir -p folder4/folder4-1/folder4-1-1`
  - explore and make sure all 6 folders above were created
2. Folder removing:
  - non-empty folders
    - try to remove **folder4** by executing `rmdir folder4/`. What's happened?
    - remove **folder4** by executing `rm -rf folder4/`
    - make sure **folder4** was deleted
  - empty folders
    - try to remove **folder1** by executing `rmdir folder1/`. What's happened?
    - remove **folder2** using `rm -rf`
    - romove **folder3**

#### 2. Working with files
Create work directory **task6** and go into it.
1. File creating: touch-way
  - create **test1** file: `touch test1`
  - explore the content of current directory, make sure **test1** was created. How big is it?

2. File creating: with **vi**
  - run `vi test2`
  - you are in Vi text editor now:
    - press `i` to enter in insert mode
    - input `Hello file`
    - press `Esc` to get in normal mode
    - enter `:wq` or `:x` to save and exit
  - let's see the content of **test2** file: `cat test2`. What can you see?
  - explore the content of current directory, how many files are there now?

3. File creating: redirection-way
  - execute `echo 'Hello, another file' > test3`
  - explore the content of current directory again. What can you see? Get the content of created file.
  - execute `echo 'Hello batman' > test3` and explore the content of **test3** file again. What you see?
  - execute `echo 'Hello joker' >> test3` and explore the content of **test3** file again. Describe what you see?

4. File creating: with **cat**
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

5. Copy, move, rename
  - create folder **task6_sub**
  - let's make a copy of **test2** file: `cp test2 test2_copy`. Explore the content of current directory, how many files are there now?
  - let's move a copied file into new folder: `mv test2_copy task6_sub/`
  - explore the content of current and **task6_sub** directory
  - rename **task6_sub/test2_copy** file: `mv task6_sub/test2_copy task6_sub/test2_new_name`. check the renaming.
  - rename **task6_sub** folder to **task*_new_name**. check the renaming.

6. Executed files
  - go to the **task6** folder and execute the **test2** file. What dod you get? Describe an error.
  - let's make this file executable:
    - rewrite the file: `echo 'echo $PATH' > test2`. Print the **test2** file content again.
    - edit **test2** with **vi** - insert `#!/bin/bash` as the first line of the file.
    - get list-view of the **test2** file: `ls -l test2`
    - execute `chmod u+x test2`
    - get list-view of the **test2** file again. What have changed?
  - now we can run **test2** by executing `./test2`. What did you get?

7. Archiving
  - go to the home directory. Explore the content of current directory and make sure there is **task6** folder here.
  - tar archives
    - let's archive this folder: `tar -czvf test.tar.gz task6/`.
    - explore the content of current directory and make sure there is **test.tar.gz** archive here.
    - explore the content of created archive: `tar -tvf test.tar.gz`
    - Unarchive **test.tar.gz** to the temp directory.
  - zip archives
    - archive **task6** folder: `zip -rp test.zip task6/`.
    - explore the content of current directory and make sure there is **test.zip** archive here.
    - explore the content of created archive: `unzip -l test.zip`
    - Unarchive **test.zip** to the temp directory
  - archive names
    - explore content type of **test.tar.gz** archive: `file test.tar.gz`
    - rename the archive by removing file extension
    - explore content type again. Has something changed?

8. Files searching
  - go to the home directory. Explore the content of current directory and make sure there is **task6** folder here.
  - try to find **passwd** file: `locate passwd`
  - let's find all task* directories in home directory: `find $HOME -name "task*" -type d`
  - let's find all test* files in home directory: `find $HOME -name "test*" -type f`
  - let's find all executed test* files in home directory: `find $HOME -name "test*" -type f -perm /a+x`
  - explore the opportunities of find command (`man find`) and find all files in home directory not older than 3 hours

9. Removing
  - go to the **task6** directory
  - remove file **test1**: `rm test1`
  - remove file **test2** without confirmation
  - remove **test3**, **test4** files without confirmation with one-line command


## Helpful Materials
- https://www.youtube.com/watch?v=TdhJbZ-yqag&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=27
- https://www.youtube.com/watch?v=g1rvmo1x4Bg&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=28
- https://www.youtube.com/watch?v=dEETXJBhCgw&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=29
- https://www.youtube.com/watch?v=9E4pHA8kUHQ&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=32
- https://www.youtube.com/watch?v=iyEVVn30iN8&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=33
- https://www.youtube.com/watch?v=k2b_5GY5gMU&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=35
- https://www.youtube.com/watch?v=X8NVOoFeMT0&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=36
- https://www.youtube.com/watch?v=RTZP0cQ2VLk&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=37
- https://www.youtube.com/watch?v=VYmKQMlPrOQ&list=PLD_mb6U5Xp95cX_CDO3Cg-p8370lPwRR2&index=38
- https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Step_by_Step_Guide/s1-managing-files.html
- https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html/Step_by_Step_Guide/s1-manipulate-current.html
- https://www.computernetworkingnotes.com/rhce-study-guide/tar-command-and-syntax-explained-with-examples.html
- https://www.computernetworkingnotes.com/rhce-study-guide/how-to-use-the-vi-and-vim-editors-in-linux.html
- https://vim-adventures.com/
