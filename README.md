# Shell-clean-sheat  🐚 🐚 🐚 🐚




Special Variable  | Description
----------------- | ------------
$0                | The filename of the current script
$n                | "n" refers to a positive number that represents the nth argument passed to the script. For example, $1 represents the first argument
$#                | Represents the number of arguments passed to the script
$*                | Represents all the arguments passed to the script
$@                | Represents all the arguments passed to the script
$?                | Returns the exit status of the last command that was executed
$!                | Holds the process ID of the last background command
$$                | Represents the process ID of the current shell. For shell scripts, this is the process ID under which the scripts run



* `compgen -c` -> will list all the commands you could run.
* `compgen -a` -> will list all the aliases you could run.
* `compgen -b` -> will list all the built-ins you could run.
* `compgen -k` -> will list all the keywords you could run.
* `compgen -A function` -> will list all the functions you could run.
* `compgen -A function -abck` -> will list all the above in one go.







# Operating system
(the core of all software)
 system software that manages computer hardware and software resources, and provides common services for computer programs.
 e.g  Microsoft windows, macOs, ***Linux**, ios
 
 ## structure of Linux

    
                ==Application Software== 📲 📟  This is all system apps and user apps 
                            ↓
                  ==Grapical Desktop Environment== 🖥
                                          ↓ ↑
                       ↓    ==GNU system Utilities==  Utilities for  ***handling files, manipulating text, managing process eg ls, find, cd, ps ...*** 
                                            ↓ ↑
                                  ===========shell================ sh, zsh, bash, ash, tcsh
                       ↓                    ↓        ↑ 
                    =============Linux Kernel=============== **memory management, process management, harware management, Filesystem management
                          ↓ ↑                    ↑ ↓   
                    ==========computer hardware============= Network device, 




