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
 system software manages computer hardware and software resources, and provides common services for computer programs.
 e.g  Microsoft windows, macOs, ***Linux**, ios
 
 ## structure of Linux

    
                ==Application Software== 📲 📟  This is all system apps and user apps 
                            ↓
                  ==Grapical Desktop Environment== 🖥
                                          ↓ ↑
                       ↓    ==GNU system Utilities==  Utilities for  (1) handling files, (2) manipulating text, (3) managing process. samples are command  ls, find, cd, ps ... 
                                            ↓ ↑
                                  ===========shell================ sh, zsh, bash, ash, tcsh
                       ↓                    ↓        ↑ 
                    =============Linux Kernel=============== (1) memory management, (2) process management, (3) harware management, (4) Filesystem management
                          ↓ ↑                    ↑ ↓   
                    ==========computer hardware============= Network device, 





> In Linux everything is a FILE 📌
>> The Linux structure is as represented but this only includes directories and files of significant note  📌

## Directory and File Structure
```
 * 📁 / -> the Root of all files and directory 
     * 📁 /boot/ ->
     * 📁  /etc/ ->
         * 📄 /etc/profile ->
         * 📄 /etc/passwd ->
         * 📄 /etc/shadow ->
         * 📄 /etc/hosts
         * 📁 /etc/init.d/
     * 📁 /home/
     * 📁 /lib/
     * 📁 /root/
     * 📁 /tmp/
     * 📁 /dev/
         * 📄 /dev/sda
     * 📁 /proc/
     * 📁 /media/
     * 📁 /sbin/
     * 📁 /bin/
     * 📁 /usr/
         * 📁 /usr/sbin/
         * 📁 /usr/bin/
         * 📁 /usr/local/
             * 📁  /usr/local/bin/
         * 📁 /usr/share/
            * 📄 /usr/share/man
            * 📄 /usr/share/doc
     * 📁 /var
         * 📁 /var/log/
         * 📁 /var/spool/
            * 📄 /var/log/spool/mail
```
       
   

