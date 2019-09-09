## Prerequizites

1. Log in to VM as devops user and run Terminal (Applications - System Tools - Terminal)

## Tasks

1. Run `top` command, explore options it provides  

2. Run top in background:
    * Suspend it with `Ctrl+Z`
    * List jobs by executing `jobs`. What is id of top process?
    * Bring top to background by executing `bg [id]`
  
3. Bring it back to foreground by running `fg [id]`

4. Suspend process and kill it using `kill -9 %[id]`

5. Run 2 top processes on the background by `top &`. What are their ids?

6. Execute `killall -9 top`. What processes have been killed?

7. Run the `ps -m` command and see what processes you have running are multi-threaded.

10. Take a look at your running processes by `ps -ef`, can you see what processes have parents?

11. Execute `ps -ejH`. Check your assumption.
