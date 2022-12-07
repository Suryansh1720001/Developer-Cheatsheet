# Linux 
Unix is now one of the most commonly used Operating systems used for various purposes such as Personal use, Servers, Smartphones, and many more. It was developed in the 1970’s at AT& T Labs by two famous personalities Dennis M. Ritchie and Ken Thompson.

## Contents

- [Architecture of Linux](#architecture-of-linux)
- [Files](#files)
- [Files Permission](#files-permission)
- [To change directory permissions in Linux, use the following](#to-change-directory-permissions-in-linux-use-the-following)
- [Linux Text Editors](#linux-text-editors)
- [Tar](#tar)
- [Zip](#zip)
- [Top Networking Commands](#top-networking-commands)
- [Process Commands](#process-commands)
- [System Control Commands](#system-control-commands)
- [Shortcuts used in Linux](#keyboard-shortcuts-for-linux)


## Architecture of Linux
- Kernel
- System Library
- Shell
- Hardware Layer
- System Utility

## Files
```sh
ls                        # list all files
ls -al                    # lists hidden files
cd <path>                 # change directory to path
cd                        # change to home
pwd                       # shows current directory
mkdir <dirName>           # create a new directory with given name
cat <fileName>            # displays the file content
cat > <fileName>          # creates a new file
rm <fileName>             # removes file with given name
du -sh *                  # list directories with their total sizes 
df -h                     # to see free disk space
mv <dirname>              # to move files and directories
mv <old_name> <new_name>  # to rename files and directories

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

5. Kate/Kwrite
Kate/Kwrite is the default text editor in KDE desktop environment. When we open a text file, it will open with Kate text editor.

```
## Tar
- Use the tar command to compress and expand files from the command line. The syntax is shown below:

### Syntax
- tar [options] [archive-file] [file or directory to be archived] 

```sh
tar -zcvf foo.txt.tar.gz foo.txt		# Create a zipped archive-file
tar -tvf foo.txt.tar.gz				# List archive files
tar -xvf foo.txt.tar.gz				# Extracting archive-file
tar -rvf foo.txt.tar.gz	foo.txt			# Add file to existing archive file


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

### Uname
- uname command is use to see system information.


### Syntex
- uname [Option]
```sh
$ uname -a 
Linux dev.linuxize.com 4.19.0-6-amd64 #1 SMP Debian 4.19.67-2+deb10u1 (2019-09-20) x86_64 GNU/Linux

Options:

-a or --all 				# Print all information  
-s or --kernal-name 			# Print the kernel name 
-n or --nodename 			# Print the network node hostname  
-r or --kernal-release 			# Print the kernel release  
-v or --kernal-verison  		# Print the kernel version  
-m or --machine 			# Print the machine hardware name  
-p or --processor 			# Print the processor type  
-i or --hardware-platform 		# Print the hardware platform  
-o or --operation-platform 		# Print the operating system  
--help  				# Display the help and exit  
--version 				# Output version info. and exit

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

## System Control Commands
- System control commands in linux are used to manage both system and service configurations, enabling administrators to manage the OS and control the status of services. There syntaxes and descriptions are listed below.

```
	Commands 							Description

-	systemctl reboot 						# Used for rebooting the server
- 	systemctl poweroff 						# To initiate a shutdown process
-	systemctl get-default 						# To display the current default display  
-	systemctl set-default graphical.target 				# To change default to GUI
-	sytemctl rescue 						# Switch to rescue mode 
-	systemctl start {servicename} 					# To start a service
-	systemctl stop {servicename} 					# To stop a service
-	systemctl restart {servicename} 				# To restart a service
-	systemctl mask {servicename} 					# Prevent a service from starting 
-	systemctl enable {servicename} 					# Enable a service
-	systemctl disable {servicename}					# Disable a service
-	systemctl is-active {servicename}				# Confirm active status
-	systemctl is-enabled {servicename}				# Confirm enabled status
-	systemctl kill {servicename}					# Kill a service with signal 15
-	systemctl kill -s 9 {servicename}				# To force the system to kill a service immediately
-	systemd-analyze							# For management and analysis service
-	systemd-analyze blame						# Display service start times
```

## Keyboard shortcuts for Linux

### General Linux Shortcuts

| Command | Description |
|---------|-------------|
| `Ctrl + C` | Copy any highlighted text, image, or some other object to the clipboard. |
| `Ctrl + V` | Paste copied text, image, or some other object from the clipboard. |
| `Ctrl + X` | Cut highlighted text, image, or some other object. |
| `Ctrl + S` | Save the currently opened file. |
| `Ctrl + N` | Create a new file. |
| `Ctrl + Z` | Undo the last action. |
| `Ctrl + Q` | Quit the application in focus. |
| `Ctrl + Alt + F1` to `F6` | Switch to a virtual console. |
| `Ctrl + Alt + F7` | Switch to the first graphical terminal. |

### GNOME Keyboard Shortcuts

| Command | Description |
|---------|-------------|
| `Super` | Enter the Activities Overview. |
| `Alt + Tab` | Cycle between running applications. |
| `Alt + Shift + Tab` | Cycle between running applications in the opposite direction. |
| `Alt + F1` | Open the Applications menu. |
| `Alt + F2` | Open a floating command prompt. |
| `PrtSc` | Take a screenshot of the entire screen. |
| `Alt + PrtSc` | Take a screenshot of the window in focus. |
| `Ctrl + Alt + Arrow keys` | Switch between workspaces. |
| `Ctrl + Alt + D` | Minimize all windows to show desktop. |

### KDE Keyboard Shortcuts

| Command | Description |
|---------|-------------|
| `Super` | Open the Application Launcher. |
| `Alt + Space` | Bing up the Command Interface. |
| `Ctrl + Esc` | Open the System Activity utility. |
| `Super + Alt + Arrow keys` | Switch between windows. |
| `Ctrl + F1 to F4` | Switch between virtual desktops. |
| `Super + Tab` | Cycle between running applications. |
| `Super + Shift + Tab` | Cycle between running applications in the opposite direction. |
| `Ctrl + Alt + L` | Lock the current session. |
| `Ctrl + Alt + Shift + Del` | Instantly log out without confirmation. |
| `Ctrl + Alt + Shift + Page Up` | Instantly reboot without confirmation. |

### Xfce Keyboard Shortcuts

| Command | Description |
|---------|-------------|
| `Super + P` | Open Xfce display settings. |
| `Alt + F2` | Open a command prompt. |
| `Ctrl + Alt + Arrow keys` | Move between virtual desktops. |
| `Alt + Tab` | Cycle between running applications. |
| `Alt + Shift + Tab` | Cycle between running applications in the opposite direction. |
| `Alt + F4` | Close the window in focus. |
| `Alt + F10` | Maximize the window in focus. |
| `Ctrl + Alt + D` | Minimize all windows to show desktop. |
| `Ctrl + Alt + Del` | Lock the current session. |
| `Ctrl + Esc` | Display context menu. |

### LXDE Keyboard Shortcuts

| Command | Description |
|---------|-------------|
| `Ctrl + Alt + T` | Launch Terminal. |
| `Shift + Alt + Arrow keys` | Move the window in focus between virtual desktops. |
| `Ctrl + Alt + Arrow keys` | Move between virtual desktops. |
| `Alt + Tab` | Cycle between running applications. |
| `Alt + Shift + Tab` | Cycle between running applications in the opposite direction. |
| `Alt + F4` | Close the window in focus. |
| `Alt + Esc` | Hide the window in focus. |
| `Super + D` | Minimize all windows to show desktop. |
| `Super + E` | Launch the default file browser. |
| `F11` | Toggle Fullscreen. |

### Cinnamon Keyboard Shortcuts (Linux Mint)

| Command | Description |
|---------|-------------|
| `Ctrl + Alt + Down` |Show all currently running applications on the selected workspace. |
| `Ctrl + Alt + Up` |Show running applications across all workspaces. |
| `Alt + Tab` |Cycle between running applications. |
| `Shift + Alt + Tab` |Cycle between running applications in the opposite direction. |
| `Alt + F2` |Open a command prompt. |
| `Alt + F4` |Close the window in focus. |
| `Super + L` |Open the Cinnamon Debugger. |
| `Super + D` |Minimize all windows to show desktop. |
| `Ctrl + Super + Arrow keys` |Span the window in focus to a border. |
| `Shift + Ctrl + Alt + Left` or `Right Arrow` |Move the window in focus to the workspace on the left or right. |

### Bash Keyboard Shortcuts

| Command | Description |
|---------|-------------|
| `Ctrl + A` | Go to the beginning of the selected line. |
| `Ctrl + E` | Go to the end of the selected line. |
| `Ctrl + K` | Cut the part of the selected line after the cursor and copy it to the clipboard. |
| `Arrow Up` | Previously used command. |
| `Alt + B` | Move the cursor back one word. |
| `Alt + F` | Move the cursor forward one word. |
| `Ctrl + L` | Clean the current screen. |
| `Ctrl + J` | Enter the Newline control character. |
| `Ctrl + R` | Search in your Bash history. |
| `Ctrl + G` | Exit the history searching mode. |

## Ubuntu Keyboard Shortcuts

| Command | Description |
|---------|-------------|
| `Super` | Open Activities. |
| `Alt + F2` | Open a command prompt.|
| `Alt + Tab` | Cycle between running applications.|
| `Super + Arrow keys` | Snap the window in focus to a border.|
| `PrtSc` | Take a screenshot of the entire screen.|
| `Alt + PrtSc` | Take a screenshot of the window in focus.|
| `Shift + PrtSc` | Take a screenshot of a selected area on the screen.|
| `Ctrl + Alt + T` | Launch Terminal.|
| `Super + L` | Lock the current session.|
| `Super + D` | Minimize all windows to show desktop.|

### Firefox Keyboard Shortcuts

| Command | Description |
|---------|-------------|
| `Backspace` | Go back. |
| `F5 or Ctrl + R` | Reload the current page. |
| `Ctrl + P` | Print the current page. |
| `Ctrl + S` | Save the current page. |
| `Ctrl + F` | Find text on the current page. |
| `Ctrl + K` | Bring the search bar into focus. |
| `Ctrl + W` | Close the current tab. |
| `Ctrl + N` | Open a new tab. |
| `Ctrl + Shift + P` | Open a new private window. |
| `Ctrl + Shift + Q` | Exit Firefox. |

### ChromeOS Keyboard Shortcuts (Chromebook)

| Command | Description |
|---------|-------------|
| `Ctrl + Shift + L` | Lock the current session. |
| `Ctrl + Shift + Q` | Log out from the current session. |
| `Alt + 1 to 8` | Launch an application from the taskbar. |
| `Alt + [` or `]` | Dock the window in focus to the left or right side of the screen. |
| `Ctrl + F5`| Take a screenshot of the entire screen. |
| `Ctrl + Shift + F5` | Take a screenshot of a selected area on the screen. |
| `Shift + Alt + M` | Open the Files app. |
| `Shift + Alt + N` | Display notifications. |
| `Ctrl + Alt +` | Display all keyboard shortcuts. |
| `Shift + Esc` | Open the Task Manager. |
