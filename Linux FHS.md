# General Linux File System Hierarchy (FHS)

## /bin

**Name:** Binaries  
**Notes:**
* Essential user command binaries resdide here.
* These are available for all users.
**Example:** Things like _ls_ and _cat_ are here.

## /sbin

**Name:** System binaries  
**Notes:** 
* Only system admin can edit.
* Contains binary executables.
**Example:** reboot, fdisk, ifconfig, swapon, etc.

## /boot

**Name:** Boot  
**Notes:**
* Contains everything OS needs to boot.
* Kernel initrd, vmlinux, GRUB files are located here.
**Example:** initrd.img-2.6.32-24-generic


## /dev

**Name:** Devices  
**Notes:** 
* Where devices files live.
* These include terminal devices, USB, or any device _attached_ to your system.
**Example:** Here you'll find hardware like: disks and their partitions, cameras, etc. Files such as /dev/tty1 too.


## /etc

**Name:** Etcetera  
**Notes:** 
* For system wide configurations of apps.
* Contains files required by all programs.
* This also contains startup and shutdown shell scripts used to start/stop individual programs.
**Example:** -

## /home

**Name:** Home  
**Notes:** 
* For individual users.
**Example:** -


## /lib

**Name:** Library  
**Notes:** 
* Contains files applications that can be use to perform various functions.
* Libraries essential for the binarier in /bin and /sbin are here.
* Library filenames are either in ld\* or lib\*.so.\* format.
**Example:** -


## /mnt

**Name:** Mount  
**Notes:** 
* Where you'd find mounted drives like USB-disks, external hard drives, etc.
* Temporary mount directory where sysadmins can mount filesystems. 
**Example:** -


## /media

**Name:** Media  
**Notes:** 
* Where you'd find mounted drives like USB-disks, external hard drives, etc.
* Temporary mount directories for removable devices.
**Example:** -

## /opt

**Name:** Optional  
**Notes:** 
* Optinal application software packages.
* Where manually installed software from vendors resides. And also repo packages.
* Contains add-on applications.
**Example:** -


## /proc

**Name:** Processes  
**Notes:** 
* Virtual filesystem providing process and kernel information as files. In Linux, this corresponds to a "procfs mount".
* Where you'd find pseudo files that contain information about running system processes and system resources.
**Example:**
* System monitor --> Process ID. That folder number exists in /proc
* CPU information
* Uptime information

## /root

**Name:** Root  
**Notes:** 
**Notes:** 
* Root user's home folder. 
* You need root permission to access.
**Example:** -


## /run
**Name:** Run  
**Notes:** 
* It's a "tempfs" filesystem: runs in RAM. Thus, everything here is gone when system shuts down.
* Stores volatile runtime data.
**Example:** -

## /snap
**Name:** Snap  
**Notes:** 
* Where snap packages reside. These are mainly used by Ubuntu.
**Example:** -


## /srv
**Name:** Service  
**Notes:** 
* Site-specific data served by this system, such as data and scripts for web servers, etc.
* Where server data for sites is stored  
**Example:** -


## /tmp
**Name:** Temporary  
**Notes:** 
* Files that are temporarily used by applications.
* Files under this directory are deleted when system is rebooted.
**Example:** Autosave


## /sys

**Name:** System  
**Notes:** 
* Interact with kernel. 
* Similar to /run in that it's temporary.
**Example:** - 

## /usr

**Name:** User (but also referred to as Unix Service Resource)  
**Notes:**
* Contains the majority of user utilities and applications.
* Apps here are considered non-essential for system operations.
* /usr/bin contains binary files for user programs
* /usr/sbin contains binary files for system admins
* /usr/lib contains libraries for /usr/bin and /usr/sbin
* /usr/local contains user programs that you install from source. 
* /usr/src holds the Linux kernel sources, header-files, and documentation. 
**Example:** Some good to know sub-folders are /usr/local, /user/share, /usr/src
