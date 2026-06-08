# Introduction-to-Linux-for-replacing-Windows
A complete beginner friendly guide to us Linux as a daily driver.
The guide contains some of the main concepts and focuces on the practical aspect of using Fedora KDE Linux.

### Linux intro:

- **what is linux** :  a Kernel
	- what is a kernel: 

- **what are the benefits compared to windows**: 
	- faster
	- more battery life
	- more security
	- full control
	- opens the door for high paying jobs
	- real understanding of how computer and programs function  
	- reliability

- **limitations**:
	- no adulbi programs (not the easy way at least)
	- some online games won't work (a decision made by the developers)
	- cutting edge Nvidia drivers features don't work
------------------------------------------------------------------------
### Linux destros and flavors:
A Linux distribution bundles the Linux kernel with a collection of software, such as system utilities, libraries, and applications. It often includes a package manager for installing and managing software, and a desktop environment for the graphical user interface (GUI). Essentially, a distro is a complete, ready-to-use operating system built around the kernel.



- **Debian**: 
  is a highly influential operating system composed entirely of free and open-source software. With a development history spanning decades, it is one of the oldest and most respected community-driven projects.


- **Red Hat Enterprise Linux**:  
  often called RHEL, is a commercial Linux distribution developed by Red Hat for the corporate market. It is a leading choice for an **enterprise linux** operating system, built to provide long-term stability, security, and professional support. While RHEL requires a subscription for use in production, Red Hat provides its source code freely, which forms the basis for other distributions.     
  -The primary appeal of RHEL lies in its suitability for **enterprise linux systems**. It is designed for mission-critical workloads, offering a predictable release cycle, long-term support (up to 10 years or more), and a vast ecosystem of certified hardware and software. This makes it a reliable foundation for servers, cloud computing, and containerized applications in large-scale corporate environments.
##### Flavores:

- **Fedora**: 
  Sponsored by Red Hat, the **Fedora** Project is a community-driven initiative that develops and maintains a free and open-source operating system. It is known for integrating cutting-edge technologies and providing a modern, user-friendly experience. Think of Fedora as an equivalent to Ubuntu, but built upon a Red Hat foundation instead of Debian.

- **Ubuntu**: 
  Ubuntu is one of the most popular and widely-used Linux distributions, making it an excellent entry point for anyone looking to **get started with Ubuntu**. Developed by Canonical, it is built on the robust foundation of **Debian** and is known for its user-friendly design and strong community support.

- **Arch**:
  Unlike distributions with scheduled releases, Arch uses a rolling-release model. This means you receive continuous, incremental updates, ensuring your system always has the latest stable software without needing a major version upgrade.
  -The core philosophy of **Arch** is simplicity, modernity, and user-centrality. This approach requires users to get their hands dirty to understand the system's functions, but in return, it offers complete and total control over the operating system.
  -If you want a minimalist operating system and truly want to understand the inner workings of Linux, Arch is an excellent choice.

------------------------------------------------------------------------
### Desktop environments:

- **KDE**:

- **Gnom**:

- **Cinemon**:

- others:

------------------------------------------------------------------------
### First time installation of Fedora KDE: 

- installing fedora
- enabling 3rd party packages
- updating the system
- installing NVIDIA drivers  

------------------------------------------------------------------------
### Configuring the system sittings:

- mouse & touchpad
	- touchpad 
		- (❌) Enable pointer accelertion
		- (✔️) Inverted scrol direction
		- (✔️) Tap to click
	
- Keyboard
	- Keyboard
		- Layouts: add the english and arabic languages
	- shortcuts
- Display & Monitor
	- Display edges
- Disks & Cameras
	- Device Auto-Mount
- Wi-Fi & Network
	- Wi-Fi & Networking: you can see the saved wifi passwords
- Default Applications
- Window Management
	- Window Behaviour
		- Focus
			- Window activation policy
- Activites
- Screen Locking / Power Managment : to change the screen sleep/Lock time

------------------------------------------------------------------------
### The applications repositories and package managers:

A Linux system is composed of many software components, such as web browsers, text editors, and media players. These components are known as packages, and they are typically managed by a package manager, which handles the installation, update, and removal of software. Understanding this process is a fundamental part of the **best way to learn Linux**.

##### What is a Package Repository
A package repository is a central storage location for software. These repositories, hosted on servers across the internet, contain curated collections of Linux packages, eliminating the need for manual downloads and installations. This system is a cornerstone of modern Linux package management, providing a streamlined and secure way to manage software.


- **.rpm**: Red Hat Package Manager
- **dnf**:
- **apt**: Advanced Package Tool
- **.deb**:

Just like `.exe` is a single executable file, so is `.deb` and `.rpm`. You normally wouldn't see these if you use package repositories, but if you directly download packages, you will most likely get them in these popular formats. Obviously, they are exclusive to their distributions: `.deb` for Debian-based and `.rpm` for Red Hat-based.

- **snap**:
- **pacman and AUR**:
- **Flatpack**:
- **appimage**:

- **yum**: ?


------------------------------------------------------------------------

### Everyday applications on Linux:

- Dolphin
- Brave
- Heroic / Lutris / steam
- system monitor
- KDE integration extension

------------------------------------------------------------------------
### Productivity applications:

- FreeCAD 
- KiCad
- Krita
- LibreOffice
- PDF Arrange #Exclusive
- davinci resolve

------------------------------------------------------------------------
### Powerful applications on Linux:

- Vakt-i salah
- Bottles
- Filelight
- Flatseal
- Gear lever
- KDE connect  #Exclusive 
- LocalSend
- Obsidian
- pigment
- SSH pilot #Exclusive 
- TeXstudio

##### Ones new to me:
- upscayl
- buzz
- frog
- foliate
- 


------------------------------------------------------------------------
### Understanding the file structure:

#### Filesystem Hierarchy

You are likely becoming familiar with the directory structure on your system. Most Linux distributions organize their filesystems according to the **Linux File System Hierarchy** (FHS) Standard. This standard ensures that files are stored in predictable locations, making systems more consistent.

To see the top-level directories, run the command `ls -l /`. While your system might have minor differences, the core **linux file hierarchy structure** will be very similar to the one described below.

###### The Root Directory

- `/` - This is the root directory, the starting point for the entire filesystem. Every single file and directory on your system is located under this directory.

###### Essential System Directories

The **file hierarchy in linux** includes several directories critical for the system's operation.

- `/bin` - Contains essential command-line programs (binaries) available to all users, such as `ls`, `cp`, and `mv`.
- `/sbin` - Holds essential system binaries, which are primarily intended for system administration and can typically only be run by the root user.
- `/etc` - This is the core system configuration directory. It contains configuration files for the operating system and installed applications, but it should not contain any executable binaries.
- `/lib` - Contains essential shared library files that system binaries in `/bin` and `/sbin` depend on to function correctly.
- `/boot` - Stores the files required for the system's boot process, including the Linux kernel and the boot loader files.

###### User and Application Data

- `/home` - Contains personal directories for each user. This is where you store your documents, application settings, and other personal files.
- `/root` - The home directory for the root user, separate from the `/home` directory to ensure the root user can log in even if `/home` is unavailable.
- `/opt` - Reserved for optional or third-party application software packages.
- `/usr` - This directory contains user-installed software and utilities. Despite its name, it generally does not hold individual user's home files. It has its own sub-directory structure, such as `/usr/bin` for non-essential user binaries and `/usr/local` for software compiled from source.

###### Dynamic and Temporary Data

- `/var` - Stands for "variable" and stores files that are expected to change in size and content, such as system logs (`/var/log`), caches, and spool files.
- `/tmp` - A world-writable space for storing temporary files. Files in this directory are often deleted upon system reboot.
- `/run` - Contains information about the running system since the last boot, such as process IDs (PIDs) and other runtime data.

###### Device and Mount Points

- `/dev` - Contains special device files that represent hardware components like hard drives, terminals, and input devices.
- `/media` - A standard mount point for removable media like USB drives, SD cards, and CD-ROMs.
- `/mnt` - A generic mount point for temporarily mounting filesystems.

###### System Information

- `/proc` - A virtual filesystem that provides real-time information about currently running processes and kernel parameters.
- `/srv` - Intended for site-specific data served by the system, such as files for a web server.

------------------------------------------------------------------------

