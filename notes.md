# QA Linux Command Line Fundamentals notes

## Connecting to the Linux Virtual Machine
- Windows App in Mac dock
- Add PC - enter URL & Friendly name
- Go to Devices and double click on PC
- Log into Linux VM

## Introduction to the Linux Desktop
- Use Terminal

## File System Navigation
- ls: list files in directory
- cd ./Documents: move to Documents directory
- cd ..: move back one directory to root@localhost
- mkdir files: creates a directory within current directory and takes name as parameter

## File Modification
- touch hello.sh: creates a new file called hello.sh, .sh file extension is for Bash files
- nano hello.sh: uses nano text editor to edit Bash file
- Bash - Command X to exit, Y to save changes, Enter to confirm file-name
- ls -l: -l flag tells ls to list the file permissions, the owner and creation date for all files and directories it lists

-rw-r--r--
- "-" dash denotes this is a file (this would be "d" for a director)
- "rwx" for the file owner, "-" means the permission is not set
- "r" denotes the permission to read
- "w" denotes the permission to write
- "x" denotes the permission to execute

- chmod +x hello.sh: sets "x" permission for the file owner, meaning you can run it; file name has also changed to green acting as a visual indicator the file is executable

- ./hello.sh: run the file using this command

## Creating User Accounts
- adduser user: create a user called "user"
- passwd user: change password for "user"
- usermod -aG sudo user: add "user" to sudo group; aG denotes to usermod to add "user" to sudo
- su: command elevates the user to root privileges for that entire Terminal session
- sudo: command is more secure and can be put before any command that requires root privileges to elevate the user to root for that command only

## Extracting Information and Downloading Files
- grep -a 'user root' /var/log/auth.log: find lines of text that contain the phrase user root referencing the root account; the grep command is an extremely useful tool that finds occurrences of text in a file; /var/log is the directory where many logs of system activity are stored, auth.log logs actions taken by users that require authorization like logging in or using elevated privileges.
- grep -a 'user root' /var/log/auth.log | wc -l: while having the full list of authorization logs for root can be useful, you may also want to know the number of these logs. This can be achieved using a technique called piping wherein you can use the | character (known as pipe) to feed the results of one command into another.
- wget https://www.example.com -O webpage.html: download a file from the internet. The "-O" command names the file webpage.html.
- firefox webpage.html: verify the file downloaded correctly, use this command to open Firefox to view.

## Additional Useful Commands
- apt: package manager and is how Debian-based Linux systems download programs.
- apt install: command takes the name of the program to download as an argument and installs it. To do this you will need to know the name of the package as it appears in the apt databases.
- apt search: command lets you search the apt databases for packages, this is useful if you know the name of a program but do not know its exact apt name.
- man: command takes a command as an argument and shows the manual page for that command. This allows you to check the usage of commands you are not familiar with.
- ps: command shows all the processes running along with their process ID. This is similar to the Task Manager on Windows.
- kill: command takes a process ID as an argument and ends that process.
- &: operator instructs a command to be run in the background. This is useful as some commands will not allow you to use the terminal while they are running, the & operator instructs the command to run in the background, allowing you to continue using that Terminal window.
- top: command shows a list of processes running, but also shows additional information including their usage of the processor.
- q: to exit the window it displays.