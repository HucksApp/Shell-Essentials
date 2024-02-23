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
     * 📁 /boot/ -> This is where the Linux kernel and boot loader files are kept. The kernel is a file called vmlinuz.
     * 📁  /etc/ -> System configuration files directory
         * 📄 /etc/profile -> 
         * 📄 /etc/passwd -> The passwd file contains the essential information for each user. This is where user accounts are defined.
         * 📄 /etc/shadow ->
         * 📄 /etc/hosts -> This file lists the network host names and IP addresses that are known to the system.
         * 📄 /etc/fstab -> Contains a table of devices that get mounted when the system boots. This file defines the system's disk drives
         * 📁 /etc/init.d/ -> This directory contains the scripts that start various system services at boot time.
     * 📁 /home/ -> home directory, where Linux creates user directories
     * 📁 /lib/ -> The shared libraries (similar to DLLs in that other operating system)
     * 📁 /root/ -> This is the superuser's home directory.
     * 📁 /tmp/ -> Directory in which runing programs can write their temporary files.
     * 📁 /dev/ -> Device directory, where Linux creates device nodes for  devices that are available to the system, In Linux (like Unix), devices are treated like files
         * 📄 /dev/sda -> the first hard drive
         * 📄 /dev/fd0 -> the first floppy disk drive
     * 📁 /proc/ -> process directory, where current hardware and process information is stored It is entirely virtual. The directory contains little peep holes into the kernel itself.
         * 📄 /proc/cpuinfo -> tell you what the kernel thinks of the system's CPU
     * 📁 /mnt/ -> mount directory, common place for mount points used for removable media
     * 📁 /media/ -> media directory, a common place for mount points used for removable media
     * 📁 /opt/ -> optional directory, often used to store third-party software packages and data files
     * 📁 /run/ -> run directory, where runtime data is held during system operation
     * 📁 /sys/ -> system directory, where system hardware information files are stored
     * 📁 /srv/ -> service directory, where local services store their files
     * 📁 /sbin/ -> super user system binary directory,  contain system programs for system administration (super User only programs)
     * 📁 /bin/ -> system Binary directory, where many GNU utilities are stored
     * 📁 /usr/ -> user binary directory, user-level utilities and data files are stored
         * 📁 /usr/sbin/ -> super user binary directory, contain user programs for system administration (super User only programs)
         * 📁 /usr/bin/  -> user binary directory, contains applications for the system's users.
         * 📁 /usr/local/ -> local system directory, contain all user installed programs that is not part of the official distribution
             * 📁  /usr/local/bin/ -> local system user binary directory, contains binary files of user installed programs 
         * 📁 /usr/share/ -> user shared programs
            * 📁 /usr/share/man/ -> The man pages are kept here.
            * 📁 /usr/share/dict -> Dictionaries for the spelling checker that comes with Linux
            * 📁 /usr/share/doc/ -> Various documentation files in a variety of formats.
     * 📁 /var -> Directory contains files that change as the system is running.
         * 📁 /var/log/ -> Directory that contains log files. These are updated as the system runs, recording information such as the systems health
         * 📁 /var/spool/ -> This directory is used to hold files that are queued for some process, such as mail messages and print jobs
            * 📄 /var/log/spool/mail -> stores mail messages
```
       
   

