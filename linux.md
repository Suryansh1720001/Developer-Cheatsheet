# Linux 
Unix is now one of the most commonly used Operating systems used for various purposes such as Personal use, Servers, Smartphones, and many more. It was developed in the 1970’s at AT& T Labs by two famous personalities Dennis M. Ritchie and Ken Thompson.

## Architecture of Linux
- Kernel
- System Library
- Shell
- Hardware Layer
- System Utility

## Files
```sh
ls               # list all files
ls -al           # lists hidden files
cd <path>        # change directory to path
cd               # change to home
pwd              # shows current directory
mkdir <dirName>  # create a new directory with given name
cat <fileName>   # displays the file content
cat > <fileName> # creates a new file
rm <fileName>    # removes file with given name
du -sh *         # list directories with their total sizes 
df -h            # to see free disk space

```

## Files Permission
```sh
ls -l                              	# to show file type and access permission
r                                  	# read permission (4)
w                                  	# write permission (2)
x                                  	# execute permission (1)
chown <user>                       	# for changing the ownership of a file/directory
chown <user>: <group> <fileName>   	# change the user as well as group for a file or directory
chmod <mode> <filename>			# change the permissions of a file/directory

```

## To change directory permissions in Linux, use the following:
```sh
chmod +rwx                               #filename to add permissions.
chmod -rwx                               #directoryname to remove permissions.
chmod +x                                 #filename to allow executable permissions.
chmod -wx                                #filename to take out write and executable permissions.
```
## Linux Text Editors 

```sh
1.Vi/VIM editor
  Vim editor is one of the most used and powerful command-line based editor of the Linux system. 
  By default, it is supported by most Linux distros. It has enhanced functionalities of the old Unix Vi editor

2.Nano editor
Nano is a straight forward editor. It is designed for both beginners and advanced users. It has many customization features.

3. Gedit editor
Gedit editor is the default editor for the GNOME desktop environment. When we open a file, it will open with the Gedit editor.

4.Sublime Text
The sublime text editor is also one of the most popular IDE-based text editors. It is used as a development environment tool more than a text editor.

```
## Tar
- Use the tar command to compress and expand files from the command line. The syntax is shown below:

### Syntax
- tar [options] [archive-file] [file or directory to be archived] 

```sh
tar -zcvf foo.txt.tar.gz foo.txt		# Create a zipped archive-file
tar -tvf foo.txt.tar.gz				# List archive files
tar -xvf foo.txt.tar.gz				# Extracting archive-file

Options:
-c 	# Creates Archive 
-x 	# Extract the archive 
-f 	# creates archive with given filename 
-t 	# displays or lists files in archived file 
-u 	# archives and adds to an existing archive file 
-v 	# Displays Verbose Information 
-A 	# Concatenates the archive files 
-z 	# zip, tells tar command that creates tar file using gzip 
-j 	# filter archive tar file using tbzip 
-W 	# Verify a archive file 
-r 	# update or add file or directory in already existed .tar file
```
## Zip
- To compress a file , zip command is use. The syntax is shown below:

```sh
### Syntax
- zip [options] [archive-file] [file or directory to be archived]

Options:
–d      # Remove a specific file from zip
-m      # Deletes the original files after zipping
-r      # recursively zip from a folder
-u      # Add new file in zip
-v      # Show files in zip 
```

## Top Networking Commands
- Linux networking commands are widely used to analyze, maintain & troubleshoot the network(s) connected to that system

```

      **Command**                                                   **Functionality**
    
    - ping [ip_addr/hostname]                                   # check the connectivity between the 2 devices(host/server)
    - ifconfig [options] [interface]                            # configure the kernel-resident network interfaces
    - ip [options] OBJECT {COMMAND | help}                      # to show/manipulate routing, devices and tunnels
    - traceroute [options] host_address [pathlength]            # displays the route a packet takes to reach destination
    - netstat [options]                                         # monitoring incoming & outgoing network connections
    - ss [options] [filter]                                     # used to dump socket statistics  
    - dig [server] [name] [type]                                # retrieve information about DNS name servers
    - nslookup [options]                                        # retrieve information from DNS name server/used to DNS lookup
    - arp [-v] [-i if] [-H type] -a [hostname]                  # displays the ARP(Address Resolution Protocol) cache
    - curl [options] [URL]                                      # transfer data to or from a server using various protocol
    - wget [options] [URL]                                      # used to download files from the server without being logged on
    - tcpdump [options] [interface]                             # capture and analyze the incoming & outgoing packets
    - host [-aCdlriTWV] [-c class] [-N ndots] [-t type] 
    [-W time] [-R number] [-m flag] hostname [server]           # used to find the IP address from hostname or vice-versa
    - hostname -[options] [file]                                # obtain the DNS name and set the system's hostname/NIS domain name
    - whois [hostname]                                          # displays who is the owner of the domain and more info

```



## Process Commands
- Process commands in linux are used to manage the processes running on the system. There syntaxes and descriptions are listed below.

```
	Commands 							Description

-	top 								# Used to get the details of all active processes
- 	bg 									# Send a process to the background
-	fg 									# To bring a stopped process in the foreground & run  
-	ps 									# List all running processes for a user with appropriate permissions
-	ps <PID> 							# Displays the status of the process with PID <PID> 
-	pidof 								# Returns the PID of a particular process
-	kill <PID> 							# Kill the process with PID <PID>
-	nice 								# Execute a process with modified scheduling priority
-	renice 								# Modify priority of a group of processes
-	df 									# Displays the disk space available on the filesystem with each filename's argument
-	free [option]						# Summary of RAM usage, including total, used, free, shared & available memory and swap space
```
