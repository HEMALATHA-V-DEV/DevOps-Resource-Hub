# Operating System Overview

An **Operating System (OS)** is software that acts as an intermediary between computer hardware and user applications. It manages hardware resources, provides a user interface, and enables the execution of programs.

## Kernel and Shell

- **Kernel**: 
  - The kernel is the core part of the OS that interacts directly with the hardware. It manages system resources like CPU, memory, and I/O devices.
  - **Working**: The kernel operates in a privileged mode and handles low-level tasks like scheduling processes and managing memory. It communicates with hardware through drivers.

- **Shell**: 
  - The shell is the interface that allows users to interact with the OS. It can be command-line based (like Bash) or graphical (like GNOME).
  - **Interaction**: When you type a command in the shell, it sends that command to the kernel, which executes it and returns the output to the shell.

## How Software Programs Interact with the OS

When you run a program:
1. The shell receives the command to execute the program.
2. It sends the command to the kernel.
3. The kernel loads the program into memory, allocates resources, and starts executing it.
4. The program can make requests to the OS (like accessing files or network) using system calls.

## Services of the OS

- **User Services**:
  - **User Interface**: Graphical or command-line interfaces for user interaction.
  - **File Management**: Creating, reading, updating, and deleting files.
  - **Process Management**: Handling execution of programs and multitasking.
  - **Device Management**: Controlling hardware devices (printers, disks).

- **System Services**:
  - **Security**: Protecting system resources and managing user permissions.
  - **Error Detection**: Monitoring for errors and handling them appropriately.
  - **Resource Allocation**: Distributing system resources among processes.

## Types of Operating Systems

1. **Batch OS**: Executes batches of jobs without user interaction.
2. **Time-Sharing OS**: Allows multiple users to access the system simultaneously.
3. **Distributed OS**: Manages a group of independent computers and makes them appear to users as a single coherent system.
4. **Embedded OS**: Designed for specific hardware, often found in devices like appliances or cars.
5. **Real-Time OS**: Guarantees specific response times for critical tasks.

## Functions of the OS

- **Process Management**: Scheduling and executing processes.
- **Memory Management**: Keeping track of each byte in a computer's memory.
- **File System Management**: Handling the storage, retrieval, naming, sharing, and protection of files.
- **Device Management**: Coordinating and controlling hardware devices.
- **Security Management**: Protecting data and resources from unauthorized access.

## What is a System Call?

A **System Call** is a way for programs to request services from the OS. It provides an interface between a running program and the OS. System calls enable user programs to perform operations like:

- **File Operations**: Opening, reading, writing, and closing files.
- **Process Control**: Creating and terminating processes.
- **Communication**: Sending and receiving data between processes.

### Types of System Calls

1. **File Manipulation**: Operations related to files.
2. **Process Control**: Creating, terminating, and waiting for processes.
3. **Device Management**: Interacting with hardware devices.
4. **Information Maintenance**: Getting or setting system information.
5. **Communication**: Managing communications between processes.


# Linux Overview

## Meaning of Linux
Linux is an open-source operating system based on the Unix architecture. It allows users to interact with the hardware of a computer while managing system resources and running applications.

## Founded and Founder
- **Founded:** 1991
- **Founder:** Linus Torvalds

## Complete History
- **1991:** Linus Torvalds released the first version of Linux (0.01).
- **1992:** Linux became an open-source project, allowing developers worldwide to contribute.
- **1994:** Version 1.0 was released, marking its maturity as a stable operating system.
- **2000s:** Gained popularity among developers, businesses, and enthusiasts.
- **Present:** Linux is widely used in servers, desktops, and embedded systems, with distributions like Ubuntu, Fedora, and CentOS.

## Other Maintained By
Linux is maintained by a community of developers worldwide, including major organizations such as:
- **The Linux Foundation**
- **Red Hat**
- **Canonical**
- **SUSE**

## Why Linux?
- **Open Source:** Users can view, modify, and distribute the source code.
- **Cost-effective:** Generally free to use, reducing software costs.
- **Flexibility:** Can be customized for various applications, from servers to desktops.

## Advantages
- **Stability and Reliability:** Known for its stability and less frequent crashes.
- **Security:** Strong permissions model and regular security updates.
- **Community Support:** Large, active community providing support and documentation.
- **Variety of Distributions:** Users can choose from many distributions to fit their needs.
- **Performance:** Efficient resource usage, making it suitable for servers and embedded systems.
  

# 🐧 Linux Commands for DevOps Engineers

## 📂 File System Management

- **`ls`**: List directory contents.
  - **`ls -a`**: Lists all files, including hidden files (those starting with `.`).
  - **`ls -l`**: Lists files in long format, showing details like permissions, owner, size, and modification date.
  - **`ls -la`**: Combines both, listing all files with detailed information.
  - **`ls -lt`**: Displays a detailed list of files sorted by modification date, from newest to oldest.
  - **`ls -ltr`**: Lists files in long format, sorted by modification time from oldest to newest.
  - **`ls -ltrh`**: Lists files in long format, sorted by modification time from oldest to newest with human-readable file sizes.

- **`cd`**: Change directory.
  - **`cd /`**: Goes to the root directory.
  - **`cd ..`**: Moves one level up.
  - **`cd ../..`**: Moves two levels up.

- **`pwd`**: Print working directory.
- **`realpath <file_name>`**: Provides the absolute path of a specified file/directory.
- **`mkdir <directory_name>`**: Make directory.
- **`rm <file_name>`**: Remove files or directories.
  - **`rm -r <directory_name>`**: Removes non-empty directories.
  - **`rm -rf <directory_name>`**: Force remove the files & folders of a directory recursively (without confirmation).
- **`cp <source_file> <destination_file>`**: Copy files.
  - **`cp -r <source> <destination>`**: Recursively copies directories.
- **`mv <old_file_name> <new_file_name>`**: Move or rename files or directories.
- **`touch <file_name>`**: Create an empty file.
- **`cat <file_name>`**: Concatenate and display files.
- **`nano <filename>`** or **`vi`** or **`vim`**: Opens a file in the text editor for editing.

---

## 🔍 Searching and Finding

- **`find /path -name 'filename'`**: Searches for files in a specified directory and its subdirectories.
- **`locate <filename>`**: Quickly finds the location of files using a database.
- **`tail <file_name>`**: Output the last part of files.
- **`head <file_name>`**: Output the first part of files.
- **`less` / `more`**: View file contents page by page.

---

## 🔧 Text Processing

- **`awk '{print $1}' <file_name>`**: A versatile programming language for working on files.
- **`grep <pattern> <file_name>`**: Search for a pattern in files.
- **Pipe (`|`)**: Connects two commands, allowing the output of one to be used as the input for another.
- **`sed 's/old_string/new_string/g' <file_name>`**: Stream editor for filtering and transforming text.
- **`sort <file_name>`**: Sort lines of text files.
- **`tee`**: Redirect output to multiple files or displays.

---

## 🔒 File Permissions and Ownership

- **`chmod 755 <file_name>`**: Grants read, write, execute for the owner, and read/execute for group and others.
- **`chown <user>:<group> <file_name>`**: Change file owner and group.
- **`chgrp <group_name> <file_name>`**: Changes the group ownership associated with a file.

---

## 🌐 Network Management

- **`ifconfig` / `ip`**: Display or configure network interface parameters/info.
- **`ping <host_name>`**: Test network connection.
- **`netstat`**: Display network connections, routing tables, interface statistics.
- **`ssh <user>@<host>`**: Securely connect to a remote server.
- **`scp <file> <user>@<host>:/path`**: Securely copy files between hosts.
- **`wget <URL>`**: Retrieve files from the internet via HTTP/HTTPS/FTP.
- **`curl <URL>`**: Transfer data from/to a server.

---

## 📦 Disk Usage and Storage

- **`df -kh`**: Display disk space usage.
- **`du -sch`**: Estimate file space usage.

---

## 🖥️ System Information

- **`uname -a`**: Displays kernel and system information.
- **`uptime`**: Show how long the system has been running.
- **`hostname -I`**: Display the IP addresses associated with the hostname.
- **`whoami`**: Print the current user.

---

## 👥 Users and Permissions

- **`useradd <username>`**: Create a new user.
- **`passwd <username>`**: Change user password.
- **`userdel <username>`**: Delete a user account.
- **`usermod -aG <group_name> <username>`**: Modify a user account.
- **`groupadd <group_name>`**: Create a new group.
- **`groupdel <group_name>`**: Delete a group.

---

## 📦 Package Management

- **`yum install <package_name>`**: Package manager for RPM-based Linux distributions.
- **`apt-get install <package_name>`**: Package manager for Debian-based Linux distributions.

---

## ⚙️ System Maintenance

- **`cron`**: Schedule tasks to run periodically.
- **`at now + 1 hour`**: Schedule a one-time task.
- **`journalctl`**: Query and display messages from the journal.

---

## 🛠️ Service Management

- **`systemctl start|stop|restart <service_name>`**: Control the systemd system and service manager.

---

## 📊 Monitoring and Performance

- **`top`**: Displays real-time information about system processes.
- **`htop`**: Enhanced version of top, providing a more user-friendly interface.
- **`vmstat`**: Report virtual memory statistics.

---

## 📦 Compression and Archiving

- **`gzip <file_name>`** / **`gunzip <file_name.gz>`**: Compress or decompress files.
- **`zip -r <archive_name.zip> <directory_to_compress>`**: Compress a directory.
- **`tar -czvf (compress) / -xvzf(extract) <archive_name.tar.gz> <directory_to_compress>`**: Manipulate archive files.

---

## ⚙️ Process Management
- **`ps`**:Displays processes started by the current user in the current terminal session.
- **`ps -ef`**:Shows all processes running on the system.
- **`kill <process_id>`**:Gracefully terminate a process.
- **`kill -9 <PID>`**:Forcefully terminate a process.
- **`Alternatives`**: Use pkill, killall, or xkill to terminate processes by name or interactively.

---

## 📦 Package Management for RedHat
- **`sudo dnf update`** : Update installed packages.
- **`sudo dnf install <package_name>`** : Install a package.
- **`sudo dnf remove <package_name>`** : Remove a package.

---

## 🔄 Additional Commands

- **`exit`**: Cause normal process termination.
- **`logout`**: Terminates login shell.
- **`history`**: GNU History Library.
- **`lsof`**: List open files.
- **`tac`**: Display file content in reverse order.
- **`last`**: Displays a list of recent logins.
- **`date`**: Shows the current date and time.
- **`lsblk`**: List block devices.
- **`free`**: Display amount of free and used memory in the system.

---

## 📋 Additional Info for File Handling in Vim

- **`:set nu`**: Show line numbers in the left margin.
- **`Shift + G`**: Go to the end of the file.
- **`gg`**: Go to the first line of the file.
- **`:/<pattern>`**: Search for a word in the file.
- **`:wq`**: Save changes and exit Vim.
- **`:q!`**: Quit Vim without saving changes.
- **`:%s/old/new/g`**: Replace all occurrences of a word in the file.
- **`:100`**: Go to line 100 of the file.
- **`:/yum`**: Search for the word "yum" in the file.
- **`v`**: Enter visual mode to select text.
- **`dd`**: Delete the current line.
- **`yy`**: Copy the entire line.
- **`yw`**: Copy just the word.
- **`p`**: Paste copied or deleted content.
- **`u`**: Undo the last change.
- **`:X`**: Encrypt the file.
  
---

