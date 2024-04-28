# Shell-clean-sheat  🐚 🐚 🐚 🐚

![bashlogo](https://github.com/HucksApp/Shell-cln-sht/assets/58187974/d6f238e5-111f-45ee-9f0a-61305aa9dc3a)



Special Variable    | Description
------------------- | ------------
`$0`                | The filename of the current script
`$1`, `$2`, ... `$n`    | The first , second, ... arguments passed after the script name `$0`. "n" refers to a positive number that represents the nth argument passed to the script
`$#`                | Represents the number of arguments passed to the script
`$*`                | Represents all the arguments passed to the script
`$@`                | Represents all the arguments passed to the script
`$?`                | Returns the exit status of the last command that was executed
`$!`                | Holds the process ID of the last background command
`$$`                | Represents the process ID of the current shell. For shell scripts, this is the process ID under which the scripts run
`&`                | Put a job or processes to the background (background jobs)



* `compgen -c` -> will list all the commands you could run.
* `compgen -a` -> will list all the aliases you could run.
* `compgen -b` -> will list all the built-ins you could run.
* `compgen -k` -> will list all the keywords you could run.
* `compgen -A function` -> will list all the functions you could run.
* `compgen -A function -abck` -> will list all the above in one go.

-------------------------------


# Operating system ⚙️⚙️ 🖥
 system software manages computer hardware and software resources, and provides common services for computer programs.
 e.g  Microsoft windows, macOs, ***Linux**, ios
 
 ## structure of Linux ⛺️
    
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
>> The Linux structure is as represented and explained but only directories ,files, command, command options, and topics that are significant note are included here as a quick use guide.  📌

## Directory and File Structure
```
 * 📁 / -> the Root of all files and directory 
     * 📁 /boot/ -> This is where the Linux kernel and boot loader files are kept. The kernel is a file called vmlinuz.
     * 📁  /etc/ -> System configuration files directory
         * 📄 /etc/profile -> main default startup file for the bash shell on the system. All users on the system execute this startup file when they log in
         * 📁 /etc/profile.d/ -> application-specific startup files that is executed by the shell when you log in
         * 📄 /etc/passwd -> The passwd file contains the essential information for each user. This is where user accounts are defined. a special file to match the login name to a corresponding UID value
         * 📄 /etc/shadow -> File contains one record for each user account on the system, Only the root user has access
         * 📄 /etc/group -> file contains information about each group used on the system
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


-------------------------------------------------

## Linux Startups

When you log in to the Linux system, the bash shell starts as a login shell. The login shell typically looks for five different startup files to process commands from:
* /etc/profile 📄 -> main default startup file for the bash shell on the system. All users on the system execute this startup file when they log in

The other four startup files are specific for each user and can be customized for an individual user’s requirements

*  $HOME/.bash_profile  -> file first checks to see if the startup file, .bashrc, is present in the HOME directory. If it’s there, the startup file executes the commands in the .bashrc file
*  $HOME/.profile 📄 -> 
*  $HOME/.bashrc 📄 -> 
*  $HOME/.bash_login 📄 -> 



### /etc/passwd 📄
shows credentials of both ***system account*** created by linux system for services access to resources and user accounts
**Format** : 
* The login username
* The password for the user
* The numerical UID of the user account
* The numerical group ID (GID) of the user account
* A text description of the user account (called the comment field)
* The location of the HOME directory for the user
* The default shell for the user

name : usr passwd : UID : GID : title : default shell
```
$ cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
adm:x:3:4:adm:/var/adm:/sbin/nologin
lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
sync:x:5:0:sync:/sbin:/bin/sync
shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
halt:x:7:0:halt:/sbin:/sbin/halt
mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
news:x:9:13:news:/etc/news:
uucp:x:10:14:uucp:/var/spool/uucp:/sbin/nologin
operator:x:11:0:operator:/root:/sbin/nologin
gopher:x:13:30:gopher:/var/gopher:/sbin/nologin
ftp:x:14:50:FTP User:/var/ftp:/sbin/nologin
nobody:x:99:99:Nobody:/:/sbin/nologin
rpm:x:37:37::/var/lib/rpm:/sbin/nologin
owner:/dev:/sbin/nologin
mailnull:x:47:47::/var/spool/mqueue:/sbin/nologin
smmsp:x:51:51::/var/spool/mqueue:/sbin/nologin
apache:x:48:48:Apache:/var/www:/sbin/nologin
rpc:x:32:32:Rpcbind
Daemon:/var/lib/rpcbind:/sbin/nologin
ntp:x:38:38::/etc/ntp:/sbin/nologin
tcpdump:x:72:72::/:/sbin/nologin
dbus:x:81:81:System message
daemon:/:/sbin/nologin
hsqldb:x:96:96::/var/lib/hsqldb:/sbin/nologin
Blum:/home/rich:/bin/bash 
jessica:x:503:503:Jessica:/home/jessica:/bin/bash
katie:x:502:502:katie:/home/katie:/bin/bash
``` 

### /etc/shadow 📄
File contains one record for each user account on the system, Only the root user has access

**Format** : 
* The login name corresponding to the login name in the /etc/passwd file
* The encrypted password
* The number of days since January 1, 1970, that the password was last changed
* The minimum number of days before the password can be changed
* The number of days before the password must be changed
* The number of days before password expiration that the user is warned to change the password
* The number of days after a password expires before the account will be disabled
* The date (stored as the number of days since January 1, 1970) since the user
account was disabled
* A field reserved for future use

```
$ cat /etc/shadow

rich:$1$.FfcK0ns$f1UgiyHQ25wrB/hykCn020:11627:0:99999:7:::
$ 

```

### /etc/group 📄
file contains information about each group used on the system

**Format** : 
* The group name
* The group password
* The GID
* The list of user accounts that belong to the group

```
$ cat /etc/group

root:x:0:root
bin:x:1:root,bin,daemon
daemon:x:2:root,bin,daemon
sys:x:3:root,bin,adm
adm:x:4:root,adm,daemon
rich:x:500:
mama:x:501:
katie:x:502:
jessica:x:503:
mysql:x:27:
test:x:504:

$ 
```

-----------------------------------------------------------

## Text manipulation 📝

Command                     |            Description and options
----------------------------|--------------------------------------
wc
find
grep


--------------------------------

## File and Directory manipulation 📂 📄
Command                     |            Description and options
----------------------------|--------------------------------------
pwd                         | Present working Directory -> check the directory you are in the system structure `$ pwd`
cd                          | Change Directory -> change directory to the given directory name  or to home if no given `$ cd <direcrory name>` or `$ cd`
ls                          | lists the files and directories in the given directory name or current directory if no directory name `$ ls <direcrory name>` or `$ ls`
⟹                          | Options: `ls -< F R a l >  ?<direcrory name>`
⟹                          |      F -> Flag the result. directories are written like `<directory name>/` and files `<file name>`
⟹                          |      R ->  Recursive option, all directories and subdirectory is listed
⟹                          |      l -> long information, display the files and directories full information
⟹                          |      a  -> all, display all files and directories including hiddens (file hidden with `.<name>`)
cp                          | Copy -> Copying files and directories from one location in the filesystem to another  `cp  <source> <destination>`
⟹                          | Options: `cp -< i R p > <source> <destination>`
⟹                          |      i -> interactive, shell asks important modification question, as it tries to execute the given copy command
⟹                          |      R -> Recursive option, copy files in directory and all sub directory
⟹                          |      p -> keep all attributes of the file, including its access permissions, owner ....
tail
head
file
type
which
ln
mkdir
touch
rm
mv
echo
cat
sort


## File Information with ***ls***
```
$ ls -l desktop

$ drwxr-xr-x 2 christine christine 4096 Apr 22 20:37 Desktop
  ■  ■        ■    ■         ■       ■ (     ■      )  ■

■ The file type — such as directory (d), file (-), linked file (l), character device (c), or block device (b)
■ The file permissions (see Chapter 6)
■ The number of file hard links (See the section “Linking Files” in Chapter 7.)
■ The file owner username
■ The file primary group name
■ The file byte size
■ The last time the file was modified
■ The filename or directory name
```

-----------------------------------------

# Enviroment Variable manipulation

Command                     |            Description and options
----------------------------|--------------------------------------
alias
history
set
unset
export
env

-------------------------------------

## Process manipulation ⚙️⚙️🔁

Command                     |            Description and options
----------------------------|--------------------------------------
ps
bash
jobs
coproc
kill
exit
killall


---------------------------------------------------


## Compressing and Archiving data 📃 → 🗞

Command                     |            Description and options
----------------------------|--------------------------------------
zip
bzip2
gzip
compress
tar -> most used

------------------------------------------------

## Memory 💻🧠

Command                     |            Description and options
----------------------------|--------------------------------------
mount
umount
df
du


----------------------------------

## User and Group Account 👤 ♲ 👥

Command                     |            Description and options
----------------------------|--------------------------------------
useradd
userdel
usermod
groupadd
groupmod
passwd

---------------------------------------------

## ch commands

Command                     |            Description and options
----------------------------|--------------------------------------
chpasswd
chage
chfn
chsh
chmod
-----------------------------------------------------------------

# Shell Scripting


## subshell
* `(comands; commands; ...)` -> parentheses

## Shell Variable

* Defination -> `var1=value` Auto detection of data type ***int, string etc***
* Reference -> `$var1`



## command substitution
extracting the output of a shell process or commands (executed in a subshell)
* `` var1=`commands` `` -> with backticks
* `var1=$(commands)` -> with bracket

## Expression subtitution
extracting the output of a mathematical or logical expression
* `$[math expression]` -> with square bracket

 **Alternatively**
use command subtitution to extract the return of the commands evaluated expression.

* `expr` -> expr command can be use to evaluate mathematical or logical expression written in string
  `expr 1 + 5`.
* `bc` -> Bash calculator command can be used.


## Parameter Expansion
* `${parameter: value}` -> with Curly bracket


## Wildcards ⚡
* `?` question mark ->  this can represent any single character, letter/number between a-z, 0-9.
* `*` asterisk -> this can represent any number of characters (including zero, in other words, zero or more characters)
* `[ ]` square brackets -> specifies a range.
* `{ }` curly brackets -> specifies a list. terms are separated by commas and each term must be the name of something or a wildcard
* `[!]` Not in List -> specifies a Not listed match


### Output Stream redirection ⤴️🖥️
* `command > outputfile` -> `>` Write, write the stream overiding destination file  content and create destination file if not exists
* `command >> outputfile` -> `>>` Append, writes the stream appending to the destination file content 

### Input Stream redirection ⌨️⤵️
* `command < inputfile` -> `<` Write, write the stream  as input to a command specified
* `command << marker` -> `<<` The inline input redirection,  you must specify a text marker that delineates the beginning and end of the data used for input. You can use any string value for the text marker, but it must be the same at the beginning of the data and the end of the data:

## pipes ┃
* `command | command | command` -> Send the output of one command to the input of another command

## Conditional statements ⎇

## ***if*** Statemants
```
if command or test      # if condition evalutes the exit status of the command or test 
then                    # (sucess -> 0) to make decision if or not to execute the block 
  commands
else           #the else block is optional
   commands
fi
```
```
if command1 or test1
then
 commands
elif command2 or test2
then
  more commands
else              #the else block is optional
  commands
fi


if command1 or test1
then
  command set 1
elif command2 or test2
then
  command set 2
elif command3 or test3
then
  command set 3
elif command4 or test4
then
  command set 4
fi
```
------------------------------------------------------------------------

### Tests 🧪🧑‍🔬
* `test condition`  test command ->
* `[conditions]`  square bracket -> (no shell parsing for condion expressed) conditions are passed as strings
   logical and arithmetics has to be in string and option format eg  `if [ $value1 -gt 5 ]` or  `if [ $value1 \> 5 ]` : `-gt`  -> `>` : greater than. it had to be escaped in the contest since '>' in string is redirection
  * compound testing  (AND) -> all condition must be true `[ condition1 ] && [ condition2 ] ...` or  (OR) only one condition is required to be true `[ condition1 ] || [ condition2 ] ...`


### File Test 🔎📃🧪

command          |         Description
-----------------|------------------------
`-d file`        | Checks if file exists and is a directory 
`-e file`        | Checks if file exists
`-f file`        | Checks if file exists and is a file
`-r file`        | Checks if file exists and is readable
 `-s file`       | Checks if file exists and is not empty
 `-w file`       | Checks if file exists and is writable
 `-x file`       | Checks if file exists and is executable
 `-O file`       | Checks if file exists and is owned by the current user
 `-G file`       | Checks if file exists and the default group is the same as the current user
`file1 -nt file2` | Checks if file1 is newer than file2 
`file1 -ot file2` | Checks if file1 is older than file2

### String Test 🅰️🅱️🧪

command                          |         Description
---------------------------------|------------------------
`str1 = str2` or `str1 -eq str2` | Checks if str1 is the same as string str2
`str1 \< str2` or `str1 -lt str2` | Checks if str1 is less than str2 -> note without the escape character `\` 🚫 `str1 < str2` ❌  `<` is interpreted as input redirection 
`str1 \> str2` or `str1 -gt str2` | Checks if str1 is greater than str2 ->  note without the escape character `\` 🚫 `str1 > str2` ❌
`str1 -ge str2`             | Checks if str1 is greater than or equal to str2
`str1 -le str2`            |  Checks if str1 is less than or equal to str2
`str1 -ne str2`            | Checks if str1 is not equal to str2
`-n str1`                | Checks if str1 has a length greater than zero
`-z str1`                | Checks if str1 has a length of zero


## Advanced logical and mathematical expression (Test)

* `((expression))` double round bracket  -> expresssion and mathematic signs, variable are all parsed.
   * Compound expressions -> `((expression &&  expression ....))` ,  `((expression ||  expression))` , `((expression)) && ((expression )) ...` , `((expression)) || ((expression)) ...` 
* `[[expression]]` double square bracket -> expresssion and mathematic signs , variable are all parsed.
   * Compound expressions -> `[[expression &&  expression ....]]` , `[[expression ||  expression]]` , `[[expression ]] && [[expression ]] ...` , `[[expression]] || [[expression]] ...` 


## ***Case*** Statement similar to switch in other scripting Langs ⎇

```
case variable in
pattern1 | pattern2) commands1;;
pattern3) commands2;;
*) default commands;;
esac
```

-----------------------------------------


## Loop statements ♻️ 🔁

## ***for*** loop ♽
```
for var in list
do
 commands
done
```
```
for (( variable assignment ,... ; condition ,... ; iteration process ,... ))
do
 commands
done
```


## ***while*** loop  ♽

```
while test command
do
 other commands
done
```
```
while ((condition))

while [[condition]]
```

## ***Until*** loop ♽

```
until test commands
do
 other commands
done
```
```
until ((condition))

until [[condition]]
```


## ***Break*** and ***Continue***  ⌇ ↪️
* `break` -> break from immediate loop
* `continue` -> jump the rest of block execusion but continues with the loop.


-----------------------------------------


## Changing the field separator

By default, the bash shell considers the following characters as field separators:
*  A space
*  A tab
*  A newline
  
To change the field seperator set this variable -> `IFS= character : character ....`

### NOTE📌 :  For Command Chaining                                                                                   
> Use `&&` to execute one command only when the previous one succeeds.
> Use `||` to execute one command only when the previous one fails.
> Combine the above for conditional branching.
> Use `;` to join two commands when you want the second to execute no matter the result of the first one.
       

                                                       

       
   

