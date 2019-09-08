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
  



