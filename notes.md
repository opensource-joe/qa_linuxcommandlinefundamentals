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