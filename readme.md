# Linux Commands

## Shell

Shell => All the commands are fire on shell. The shell is working because it is fetching our all commands are providing the output.

### Some BRANDS in Shell

* Bourne shell (sh)
* Korn shell (ksh)
* Bourne Again shell (bash)
* zsh and many more

## Commands
- ``man 'utility_name'`` => Gives the manual of all command related to the given utilities
- ``crtl + l``  => Clear the Screen
- ``uname``     => Give the information what kind of system are you using
- ``uname -a``  => All Details regardig information
-  ``uptime``   => show how much long your system in up 

## Shell Commands
#### Basic Commands
- ``cd directory_name``    => Change Directory forward
- ``cd..``  => Change Directory backward
- ``cd``   => It gone directly to home directory
- ``mkdir`` => Create a Empty Directory
- ``ls``    => Listing all file in current Directory
- ``ls -l`` => It gives a long listing version in the current directory
- ``alias ll='ls -l'``  => This command aliasing the ll to ls -l
- ``ls -a`` => It gives all the files including hidden file
- ``vim file_name`` or ``nano file_name``   => It is default texy editor
    - In **vim** editor if you want to exit from this editor following the given steps:
        - Press the **esc** key.
        - At botton you see a **:** sign after this sign type **q**.
        - (q for quit surely it has more command).
        - Then Press **Enter** Key
- ``date`` => It gives the current Day Date
- ``cal``  => Gives Calander of the current Month.
- ``w``    => Gives How many user are logged in your system.
- ``whoami``    => It is useful to know from whoes credential you are logged in.
- ``whereis utility_name``  => Gives the path of utility where it is install.
    - It only gives the path of that program are properly install in your computer and their path are set correctly.

#### Creating and Removing Commands
- `` mkdir Directory_name`` => Creating a directory
    - "-rw-r--r" = If permission staring with **-** then it is file
    - "drwxr-xr-x" = If permission start with **d** then it is directory or folder 
- `` rm -r directory_name ``    => It delete the directory which you have to pass.
    - **-r** tends to recursively delete that folder
    - Linux thing if you are deleting a directory then chances are high that it is surely contain more files and folder inside that directory.
    - So it is deleting the recursivily deleting that folder.
- `` touch file_name.extension ``   => It create a file

- `` history`` => It gives the history of previously used commands
    - ``history > file_name.txt`` => It redirect the history of commands into the file.
- `` cat file_name ``   => It is allow us to read the file.
    - ``head`` or ``tail`` => It is also allow us to read the file but only heading part (head) and footing part(tail)  