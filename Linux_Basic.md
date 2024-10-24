

**Linux is an operating system**

I am the user and the processor will process my work and after the process give me the output as I want. When talking about Linux, Unix comes up. Uniz also is an operating system. Unix developed by Bell Labs is open-source but not free then Linus Benedict Torvalds is a Finnish and American software engineer who is the creator and lead developer of the Linux kernel. Unix Free Edition is a kernel that is called Linux like Ubuntu, Redhat, Suci Linux, etc.

**Linux architecture:**

[https://lh7-rt.googleusercontent.com/docsz/AD_4nXc61HHvHeLf4uqyNLAlMBSddPnYeBGTxbpK_ouaEfWLRMktYG1xQ39JXqaUhEHMToGkubAkikwTm_BrxisU7uxG-Lpp4whRLbWuXoqrvCreQbI8w_RQrvNwMPheHFZ0V6E7yhb5eyWUPKrGq9MFujDPeLk?key=0WyaxalrHyTNK962pWDIag](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc61HHvHeLf4uqyNLAlMBSddPnYeBGTxbpK_ouaEfWLRMktYG1xQ39JXqaUhEHMToGkubAkikwTm_BrxisU7uxG-Lpp4whRLbWuXoqrvCreQbI8w_RQrvNwMPheHFZ0V6E7yhb5eyWUPKrGq9MFujDPeLk?key=0WyaxalrHyTNK962pWDIag)

**What the kernel actually does**

The **kernel** is the core part of an operating system (OS) that manages communication between hardware and software. It acts as a bridge that allows applications and programs to interact with a computer's hardware resources such as the CPU, memory, and I/O devices (like disks, printers, and keyboards). Here's a breakdown of its main roles:

### 1\. Process Management

Memory Management

Device Management

File System Management

System Calls and Security

The kernel is like a traffic controller that ensures all parts of the system (software and hardware) work together smoothly and efficiently, all while enforcing security and isolation between processes.

**What is a shell**

Shell is like an interpreter. The shell in Linux is a powerful tool for interacting with the system, running commands, managing processes, and scripting tasks. It is the layer that users most commonly interact with when they work in a terminal environment.

Zimra all data is stored in the OPT folder and the web server content is stored in var. If I store in /root then all data is risky.

Boot- Always standard partition.

LVM-Disk management

Swap partition- Swap partition works as RAM supports RAM system cache 4 GB so RAM Swap will be 4 to 6 GB. Swap partitions are always standard. No mount point in the swap file system. Swap itself a file system type.

FQDN= Host + Domain Name

How will the data be inside the hard disk, as in Windows, everything has been done with FAT support and Linux-supported ext4 and XFS. XFS is faster but has some drawbacks.

**Command-List**

W- Shows who logged in and from where and system uptime.

**\[kakon@ansible-master ~\]$** hostnamectl

Static hostname: ansible-master

Icon name: computer-vm

Chassis: vm

Machine ID: 834222e46937458a87aabcc36773512c

Boot ID: d80020ec708a49e99f6bcf311c07cd0c

Virtualization: VMware

Operating System: CentOS Stream 8

CPE OS Name: cpe:/o:centos:centos:8

Kernel: Linux 4.18.0-553.6.1.el8.x86\_64

Architecture: x86-64

**\[kakon@ansible-master ~\]$** w

02:24:56 up 5 days, 15:36,  3 users,  load average: 0.06, 0.01, 0.00

USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT

root     tty1     -                Sun10    3days  0.11s  0.05s -bash

root     pts/0    10.10.22.14      00:28    1:56m  0.05x  0.05s -bash

root     pts/1    10.10.22.14      02:24    0.00s  0.10s  0.01s w

**7 virtual Consoles 1–6 (TTY1–TTY6)**

The load average is the last 5 minutes ago value.

Development tools used for debugging. Everything is under root but application data is not in the root folder.

!4-command number in history.

Kernel checks the command with the version

**\[kakon@ansible-master ~\]$** uname -a

Linux ansible-master 4.18.0-553.6.1.el8.x86\_64 #1 SMP Thu May 30 04:13:58 UTC 2024 x86\_64 x86\_64 x86\_64 GNU/Linux

**\[kakon@ansible-master ~\]$** uname -r

4.18.0-553.6.1.el8.x86\_64

**\[kakon@ansible-master ~\]$** date -s “01 JAN 2024 12:00:00”

If I want to set NTP then need to install chrony -y package dnf install chrony -y

**Traditional Runlevels in Linux**

There are typically 7 runlevels in the traditional SysV-style init system (0–6), each serving a specific purpose:

**File location:** /usr/lib/systemd/system

**Runlevel 0:** Halt/Shutdown

The system is completely powered off. All processes are stopped, and the machine is shut down.

Command: init 0

**Runlevel 1:** Single-user mode

Used for maintenance tasks or troubleshooting. Only a single user (usually the root user) can log in, and no networking or multi-user functionality is available. It is often used for recovery tasks or emergency fixes.

Command: init 1

**Runlevel 2:** Multi-user mode without networking

Allows multiple users to log in but without networking capabilities. In some systems, this is rarely used.

Command: init 2

**Runlevel 3:** Full multi-user mode with networking

The system runs in a multi-user mode with networking enabled, but without a graphical user interface (GUI). You can log in via the terminal and run services and servers.

Command: init 3

**\[kakon@ansible-master ~\]$** systemctl get-default

multi-user.target

**Runlevel 4:** Unused or custom

This runlevel is not typically assigned any default behavior and can be configured by the system administrator for custom purposes.

Command: init 4

If I change run level 3 to 5 then the command is systemctl set-default multi-user.target

**Runlevel 5:** Full multi-user mode with GUI

The system starts with full multi-user functionality, networking, and a graphical user interface (GUI) such as GNOME, KDE, or another desktop environment.

Command: init 5

**Runlevel 6:** Reboot

The system is rebooted. All processes are terminated, and the machine is restarted.

Command: init 6

Shutdown -C for cancel

Shutdown now

Shutdown + 10

Shutdown -r

Switch to runlevel 3 to 5

**\[kakon@ansible-master ~\]$** systemctl get-default multi-user.target

**File location** cat /etc/systemd/system/default.target

**What is file system**

A **file system** is a method and data structure that the operating system uses to manage and organize files on storage devices like hard drives, SSDs, or USB drives. It defines how data is stored, accessed, and managed on the disk, enabling you to create, read, write, and delete files and directories (folders). In essence, the file system provides a way to map raw storage space into a structure that can store files and allows for efficient data retrieval.

### **Common Types of File Systems**

Different operating systems use different types of file systems, each optimized for various use cases, performance, and compatibility requirements.

1.  **Ext4 (Fourth Extended File System)**:
    *   The default file system for most Linux distributions.
    *   Supports large volumes, journaling (to prevent data corruption), and is highly stable.
2.  **NTFS (New Technology File System)**:
    *   Used by Windows operating systems.
    *   Supports file-level security, large files, and disk compression, and it includes advanced features like journaling.
    
3.  **FAT32 (File Allocation Table 32)**:
    *   A simple file system used on older Windows systems and for cross-platform compatibility (like on USB drives).
    *   Limited to files up to 4 GB and volumes up to 8 TB, but widely supported.
4.  **exFAT (Extended File Allocation Table)**:
    *   Designed for flash storage devices (like USB drives and SD cards) where FAT32’s limitations are restrictive.
    *   Supports larger files than FAT32, without the overhead of NTFS.
5.  **APFS (Apple File System)**:
    *   The default file system used in modern macOS systems.
    *   Optimized for SSDs, with advanced features like encryption, snapshots, and cloning.
6.  **XFS**:
    *   A high-performance file system used in some Linux environments, especially for large data sets and servers.
    *   Known for its scalability and speed in handling large files and storage systems.
7.  **ZFS (Zettabyte File System)**:
    *   An advanced file system that includes features like data integrity checks, snapshots, and RAID functionality.
    *   Popular in enterprise environments for large storage arrays.

### **Components of a File System**

*   **Files**: The basic units of data storage. Files can contain data, code, or multimedia (text, programs, images, etc.).
*   **Directories**: Containers used to organize files. Directories can contain files and other directories.
*   **Inodes**: Data structures in Unix-like file systems (like Ext4) that store metadata about a file, such as its size, location on the disk, permissions, and timestamps.
*   **Superblock**: A record that contains information about the overall file system, like its size, the number of inodes, and other system-wide details.
*   **Blocks**: The fundamental unit of storage on a disk. Files are split into blocks and written to disk.

### **File System Operations**

The file system supports various operations, including:

*   **Creating a file**: Allocates space and metadata for a new file.
*   **Reading a file**: Retrieves the contents of the file from the disk.
*   **Writing to a file**: Updates the file’s contents and modifies the data stored on disk.
*   **Deleting a file**: Removes the file’s metadata and frees up the storage space.

Yum update version is dnf . Centos 8 we use dnf for the install package and for Ubuntu apt

**Standard-Unix-filesystem hierarchy**

**/root -** home directory for the root user.

\*\*/bin-\*\*essential user command binaries. like-bash, cat, chmod, cp, date, echo, grep, hostname, kill,less, mkdir, more, mount, mv, open, nano, ping, ps, pwd, rm, sh, su, tar, touch, unmount, uname, gunzip…etc

**/etc -** Configuration files for the system

Like- crontab, cups, fstab, hosts, init, hosts.allow, hosts. deny, init.d, mtab, nanorc, networks, passwd, profile, protocols, security, shells, timezone, services, issue, host. conf…etc

**/sbin -** essential system binaries

Like- fdisk, fsck, getty, halt, ifconfig, init, mkfs, reboot, route

**/usr -** read only user application support data and binaries

/usr/bin - most user commands

/usr/include - standard include files for c code

/usr/lib - obj, bin, lib files for coding and packages

/usr/local - local software

/usr/local/bin

/usr/local/lib

/usr/local/man/usr/local/sbin

/usr/local/share

/usr/share - static data sharable accross all architectures

/usr/share/man - manual pages

**/var -** Variable data files

/var/cache - application cache data

/var/lib - data modified as programmes run

/var/lock - lock files to track resources in use

/var/log - log file

/var/opt/ - variable data for installed packages

/var/spool - tasks waiting to be processed

/var/spool/cron

/var/spool/cups/

/var/spool/mail

/var/tmp - temporary files saved between reboots.

**/dev -** device files include /dev/null

**/home -** user home directories

**/lib -** libraries and kernel modules

**/mnt -**  mount files for temporary filesystems

**/opt -** optional software applications

**/proc -** process and kernel information files

1.  Root Directory ( / )

The root directory is the base of the Unix filesystem. All files and directories start from here. It's the top-most directory in the hierarchy.

1.  /bin (Binaries)

Contains essential command binaries that are needed by all users in single-user and multi-user modes.

Example: /bin/ls, /bin/cp, /bin/mv

1.  /boot

Stores files necessary for booting the system, such as the kernel and bootloader.

Example: Kernel files, GRUB configuration files

1.  /dev (Devices)

Holds device files that represent hardware components (e.g., disk drives, USB devices) or pseudo-devices like /dev/null.

Example: /dev/sda, /dev/tty

1.  /etc (Configuration Files)

Contains configuration files for the system and services. These files control how various parts of the system behave.

Example: /etc/passwd, /etc/fstab, /etc/hosts

1.  /home (User Home Directories)

Each user has a directory under /home where personal files and settings are stored.

Example: /home/user1, /home/user2

1.  /lib (Libraries)

Contains essential libraries for binaries in /bin and /sbin.

Example: /lib/libc.so.6, /lib/modules/

1.  /media and /mnt (Mount Points)

/media: Automount directory for removable media (USB drives, CD-ROMs).

/mnt: Temporary mount point for filesystems, often used for manually mounted devices.

Example: /mnt/mydisk

1.  /opt (Optional Software)

For third-party or optional software packages that are not part of the default system installation.

Example: /opt/google/chrome

1.  /proc (Process Information)

A virtual filesystem that contains information about running processes and system information. This directory is dynamic and created at boot time.

Example: /proc/cpuinfo, /proc/1234 (process ID)

1.  /root (Root User’s Home Directory)

The home directory of the root (superuser) account. It is separate from the other users' home directories.

Example: /root/.bashrc

1.  /sbin (System Binaries)

Contains essential system binaries that are typically used by the system administrator. These are required to boot, restore, recover, or repair the system.

Example: /sbin/fsck, /sbin/reboot

1.  /tmp (Temporary Files)

Used for temporary files created by programs. These files are often deleted after a reboot.

Example: /tmp/some-temp-file

1.  /usr (User System Resources)

Contains the majority of user utilities and applications. This directory is often large because it contains the bulk of installed software.

/usr/bin: Non-essential command binaries for all users.

/usr/sbin: Non-essential system binaries for administrative tasks.

/usr/lib: Libraries for binaries in /usr/bin and /usr/sbin.

/usr/share: Architecture-independent data like documentation, icons, etc.

/usr/local: Software installed locally by the system administrator (not managed by the OS package manager).

1.  /var (Variable Files)

Contains files that are expected to change in size, such as logs, databases, and spool files.

/var/log: Log files.

/var/tmp: Temporary files that should be preserved between reboots.

/var/spool: Files waiting for processing (e.g., print jobs, mail queue).

1.  /srv (Service Data)

Contains data for services provided by the system, such as web and FTP services.

1.  /sys (System Information)

A virtual filesystem that provides information about the hardware devices and system. It is closely related to /proc and is used by the Linux kernel.

1.  /run

Stores runtime data for processes started since the last boot. It is a temporary filesystem.
