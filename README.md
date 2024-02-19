# ADS Lab 01 - The command line
Authors: Anthony David, Timothée Van Hove
Date: 2024-02-19



## Task 1: What do these commands do?
> Execute the following commands in the given order. In a sentence or two, precisely
> describe what each does (English or French).
> To get documentation look up the commands using the man command. When using man , be
> careful that you are seeing the correct section (1), as the same term may be a
> command, a system call or something else. Some of the commands are shell built-ins
> ( cd , pwd , ...) which don't have manual entries, for these you can use the shell's
> help command. If the built-in help of the operating system is too confusing, try
> Google.



1. `nano newfile` Opens a file (in this case "newfile") in the nano editor. If the file does not exist, creates a new one.
2. `ls`  List information about the FILEs (the current directory by default).  Sort entries alphabetically.
  `ls -l` Use a long listing format displaying more detailed information such as the modification date and the rights
3. `cat newfile`  Displays the contents of one file without having to open the file for editing.
4. `cat /etc/hosts /etc/hostname`  Displays the content of both `/etc/hosts` and `/etc/hostname` files.
5. `ls -sh ~/.bashrc` Lists directory contents with the allocated size of each file, in blocks, in human readable format (e.g., 1K 234M 2G)
6. `pwd`
  `cd ..`
  `pwd`
7. `pwd`
  `cd .`
  `pwd`
8. `cd /home`
  `ls -l`
  `ls albert.einstein` (replace albert.einstein with your user id)
  `ls -a albert.einstein`
  `ls -d albert.einstein`
9. cd /tmp
  mkdir -p albert.einstein/bar/baz
  cd albert.einstein
  rmdir bar
  rmdir bar/baz
  rmdir bar
  Hint: rmdir 's behavior is not immediately obvious. Be careful.
10. less /usr/share/doc/bash/copyright
    less /usr/share/doc/bash/INTRO.gz
11. find ~ -name '.*' 2>/dev/null
    Hint: Break down each part of the command first.
12. cd
    mkdir bar
    touch qux
    cp qux bar
    Hint: Pay attention to bar . mv qux bar/newfile
13. uname -a
    What kind of information does this command print out?
14. history
15. sh exit bash
    exit zsh
16. sudo apt install zsh
    zsh
    exit
    What do each of these commands do?
17. apropos download
18. What happens when you type a command that does not exist, like aaaaaa ?
19. What happens when you type a command that is not installed, like ifconfig ?