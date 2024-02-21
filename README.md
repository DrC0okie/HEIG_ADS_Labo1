# ADS Lab 01 - The command line
Authors: Anthony David, Timothée Van Hove
Date: 2024-02-19



## Task 1: What do these commands do?
> Execute the following commands in the given order. In a sentence or two, precisely describe what each does (English or French).
> To get documentation look up the commands using the man command. When using man , be careful that you are seeing the correct section (1), as the same term may be a command, a system call or something else. Some of the commands are shell built-ins ( cd , pwd , ...) which don't have manual entries, for these you can use the shell's help command. If the built-in help of the operating system is too confusing, try Google.

> 1. `nano newfile` 

Opens the nano text editor with a file named "newfile". If the file doesn't exist, it will be created you once you save the changes.

> 2. `ls` 
> `ls -l`

`ls` : lists files and folders in the current directory
`ls -l` : list files and folders in the current directory in long format, including permissions, number of links, owner, group, size and last modification date.

> 3. `cat newfile`  

Displays the contents of one file "newfile" without having to open the file for editing.


> 4. `cat /etc/hosts /etc/hostname`  

Displays the content of both `/etc/hosts` and `/etc/hostname` files one after the other in the terminal.

> 5. `ls -sh ~/.bashrc` 

Lists directory contents with the allocated size of each file, in blocks, in human readable way.

> 6. `pwd`
      `cd ..`
      `pwd`

`pwd`: Displays the current working directory.
`cd ..`: Changes the current directory to the parent directory.
`pwd` : Displays the new current working directory.

> 7. `pwd`
      `cd .`
      `pwd`

`pwd`: Displays the current working directory.
`cd .`: Changes the current directory to the current directory itself, which essentially changes nothing.
`pwd`: Displays the current working directory, which has not changed.

> 8. `cd /home`
      `ls -l`
      `ls albert.einstein` (replace albert.einstein with your user id)
      `ls -a albert.einstein`
      `ls -d albert.einstein`

`cd /home`: Changes the current directory to /home.
`ls -l`: Lists files and folders in the current directory in long format.
`ls albert.einstein`: Lists the contents of the folder "albert.einstein", assuming it exists in the current directory.
`ls -a albert.einstein`: Lists all contents, including hidden files, of the "albert.einstein" folder.
`ls -d albert.einstein`: Lists the folder itself, not its contents.

> 9. `cd /tmp`
      `mkdir -p albert.einstein/bar/ba`
      `cd albert.einstein`
      `rmdir bar`
      `rmdir bar/baz`
      `rmdir bar`
      Hint: rmdir 's behavior is not immediately obvious. Be careful.

`cd /tmp`: Changes the current directory to /tmp.
`mkdir -p albert.einstein/bar/baz`: Creates a folder tree "albert.einstein/bar/baz" in the current directory.
`cd albert.einstein`: Changes the current directory to "albert.einstein".
`rmdir bar`: Attempts to delete the "bar" folder, but fails because it is not empty.
`rmdir bar/baz`: Deletes the "bar/baz" folder.
`rmdir bar`: Now succeeds in deleting the "bar" folder because it is empty.

> 10. `less /usr/share/doc/bash/copyright`
      `less /usr/share/doc/bash/INTRO.gz`

`less /usr/share/doc/bash/copyright`: Displays bash copyright information in the less viewer.
`less /usr/share/doc/bash/INTRO.gz`: Displays compressed introductory documentation for bash in the less viewer.

> 11. `find ~ -name '.*' 2>/dev/null`
      Hint: Break down each part of the command first.

Finds all hidden files (files beginning with a dot) in the user's home directory and removes error messages.

> 12. `cd`
      `mkdir bar`
      `touch qux`
      `cp qux bar`
      Hint: Pay attention to bar . mv qux bar/newfile

`cd`: Changes the current directory to the user's home directory.
`mkdir bar`: Creates a new folder named "bar".
`touch qux`: Creates a new empty file named "qux".
`cp qux bar`: Copies the "qux" file into the "bar" folder.
`mv qux bar/newfile`: Moves (renames) the file "qux" into the "bar" folder and renames it "newfile".

> 13. `uname -a`
      What kind of information does this command print out?

Displays all available system information, such as kernel name, node name, kernel version, operating system version, machine, processor, hardware platform and operating system.

> 14. `history`

Displays the order history of the current session.

> 15. `sh exit bash`
      `exit zsh`

`sh`: Starts a new Bourne shell session. This is an invitation to enter a command-line environment different from the current shell.
`exit`: Exits the current shell session, whether sh, bash, or zsh.
`bash`: Starts a new Bash shell session, another command-line environment.
`exit`: Exits the current shell session.
`zsh`: Starts a new Zsh shell session, an alternative command-line environment.

> 16. `sudo apt install zsh`
      `zsh`
      `exit`
      What do each of these commands do?

`sudo apt install zsh` : Installe le shell Zsh en utilisant le gestionnaire de paquets APT avec des privilèges de superutilisateur (sudo).
`zsh` : Démarre une nouvelle session du shell Zsh.
`exit` : Sort de la session Zsh actuelle.

> 17. `apropos download`

Search for manual pages containing the word "download". This will help you find commands related to downloading.

> 18. What happens when you type a command that does not exist, like aaaaaa ?

When you type a command that doesn't exist, such as `aaaaaa`, the shell usually returns an error message indicating that the command was not found.

> 19. What happens when you type a command that is not installed, like`ifconfig` ?

When you type a command that is not installed, such as `ifconfig`, the shell usually returns a message indicating that the command was not found. Depending on your system configuration, it may also suggest how to install the missing package.

## Extra task for pros : Editing in the command line
> The shell supports some useful keyboard shortcuts. It is worth learning them as speed up typing tremendously. Here are the most important, try to memorize them.

- `Ctrl-R` : Recherche interactive de commandes précédentes. Cela permet de rechercher une commande utilisée précédemment sans avoir à la retaper entièrement.
- `Ctrl-A` : Se déplace au début de la ligne. Cela vous permet de revenir rapidement au début sans utiliser la touche flèche gauche.
- `Ctrl-E` : Se déplace à la fin de la ligne. Utilisez-le pour aller rapidement à la fin sans utiliser la touche flèche droite.
- `Ctrl-L` : Nettoie l'affichage. Cela équivaut à lancer la commande 'clear', nettoyant votre espace de travail.
- `Ctrl-K` : Supprime tout le texte du curseur jusqu'à la fin de la ligne. C'est utile pour effacer rapidement une partie d'une commande.

> Additionally the shell has shortcuts that replace the arrow key and that allow faster typing as the hands car remain in their normal position :

- `Ctrl-P` (précédent) : Équivaut à la flèche vers le haut, permet de naviguer dans les commandes précédemment utilisées.
- `Ctrl-N` (suivant) : Équivaut à la flèche vers le bas, permet de naviguer dans les commandes suivantes.
- `Ctrl-B` (arrière) : Équivaut à la flèche gauche, permet de se déplacer vers l'arrière caractère par caractère.
- `Ctrl-F` (avant) : Équivaut à la flèche droite, permet de se déplacer vers l'avant caractère par caractère.