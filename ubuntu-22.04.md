# UBUNTU-22.04

Ubuntu is a free and open-source Linux distribution based on Debian. In this section, we will explore new features of Ubuntu 22.04.
Ubuntu is one of the most popular Linux distributions. The reason being it’s main goal is to be the most user-friendly non-geek Linux operating system out there.
- Every software either application or any operating system have its shortcomings but those softwares become best whose features outweighs their shortcomings and same is the case with the all-new Ubuntu 22.04.

### Ubuntu 22.04 Download
You can download the iso file of latest version of ubuntu from here - https://ubuntu.com/#download

### Requirements, Conventions or Software Version Used

| Category  | Requirements, Conventions or Software Version Used     |
| ------------- | ------------- | 
| System       | 64-bit PC (AMD64), see Ubuntu 22.04 system requirements        | 
| Software          | N/A        | 
| Other	    |     Privileged access to your Linux system as root or via the sudo command |
| Conventions |     # – requires given linux commands to be executed with root privileges either directly as a root user or by use of sudo command
|             | $ – requires given linux commands to be executed as a regular non-privileged user |

###  File System Navigation

| Command     | Description      | 
| ------------- | ------------- | 
| ls| 	List all the files in a directory |
| ls -l |	List all files and their details (owner, mtime, size, etc) |
| ls -a |	List all the files in a directory (including hidden files)
| pwd	| Show the present working directory |
| cd |	Change directory to some other location |
| file |	View the type of any file |

### To see system information
```sh
uname [Option]

```
| Command     | Description      | 
| ------------- | ------------- | 
| -a or --all | Print all information |
| -s or --kernal-name | Print the kernel name |
| -n or --nodename | Print the network node hostname |
| -r or --kernal-release | Print the kernel release |
| -v or --kernal-verison | Print the kernel version |
| -m or --machine | Print the machine hardware name |
| -p or --processor | Print the processor type |
| -i or --hardware-platform | Print the hardware platform |
| -o or --operation-platform | Print the operating system |
| --help | Display the help and exit |
| --version | Output version info. and exit|


### View, Create, Edit, and Delete Files and Directories
| Command     | Description      | 
| ------------- | ------------- | 
| mkdir| Create a new directory |
|touch|	Create a new, empty file, or update the modified time of an existing one |
|cat > file	| Create a new file with the text you type after |
|cat file|	View the contents of a file |
|grep|	View the contents of a file that match a pattern |
|nano file|	Open a file (or create new one) in nano text editor |
|vim file|	Open a file (or create new one) in vim text editor |
|rm or rmdir|	Remove a file or empty directory |
|rm -r|	Remove a directory that isn’t empty |
|mv	|Move or rename a file or directory |
|cp	|Copy a file or directory |
|rsync|	Synchronize the changes of one directory to another |


### Install, Update, Remove Apps and System using apt Package Manager
| Command     | Description      | 
| ------------- | ------------- |
|apt-get install| Install is followed by one or more package names desired for installation or upgrading |
|apt-get remove| Remove is used to remove a package |
|apt-get update| Update is used to Resynchronize the package index files from their sources |
|apt-get upgrade| Install the newest versions of all packages currently installed on the system from the sources enumerated in /etc/apt/sources.list |
|apt‑get dist‑upgrade| Perform the function of upgrade but may also remove installed packages if that is required in order to resolve a package conflict |


### Community Support in ubuntu-22.04

* https://ubuntu.com/support/community-support
* https://askubuntu.com/
