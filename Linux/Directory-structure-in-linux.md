Directory Structure:

1. Home Directories: The home directories for the users are located in `/home/userid`. Each user has a unique directory with their username as the name of the directory.
/root,/home/username

2. User Executable
The user executable is a program that the user can run and interact with. It should be placed in either /root or /home/username. 
/bin, /usr/bin, /usr/local/bin

3. System Executable     (not in the PATH)
   This is a program that can be run by root or other users but not by normal users. It should reside in /sbin,
   /sbin, /usr/sbin, /usr/local/sbin

4. Other Mountpoints
/proc, /sys, /dev, /mnt, /media, /var/tmp

5. Configurations:
   - /etc contains system configuration files and directories.  This is where you would put things like Apache's httpd.conf file or 
   - /etc : system configuration files and scripts for system initialization
   - /lib : shared libraries that don't need to be loaded at runtime 
   - /opt : optional packages installed by users
   - /srv : data used by servers
   - /usr/share : documentation, man pages, etc.

6. Temporary Filesystem
   The tmpfs filesystem is a RAM-based temporary file system. It provides several advantages over disk-based temporary file systems such as /tmp
   
7. Kernal Bootloader:
   The kernel boot loader is a small program that loads the kernel into memory when the computer boots up. It reads from the disk, copies
   The kernel boot loader is stored on a device separate from the root filesystem. This allows you to update or replace your operating system without affecting
   The kernel is booted from a special device called a boot loader. This device contains code that loads the kernel into memory and starts it running
   The kernel is booted from a device such as a hard disk or USB stick. This process involves loading the necessary code into memory so it 
   The kernel is loaded from here during booting. It contains code necessary to load other components of the operating system. Once the kernel has finished
   The kernel bootloader is usually stored on a separate partition or device from the root filesystem. It loads the initial RAM disk (initrd), /boot

8. Server Data:
   /var : variable data storage area
   /home : home directory of all users
   /tmp : temporary file space 
   /var/log : log files from running programs
   /var/spool : spooling data  for printing systems
   /var/mail : mailboxes for user accounts 
   /var/www : web server document root 
   /srv

   9. System information:
      /proc : a virtual filesystem containing information about running kernel objects
      /sys : a virtual filesystem containing information about the operating system such as CPU usage, memory statistics, hardware identification
      /sys : a virtual filesystem containing information about the hardware
             such as CPU type, memory size, disks, network devices, etc.
             /proc, /sys are read-only on most Unix-like operating systems.
             
10. Utilities & Tools:
    /usr/bin : standard utilities like ls, cat, cp, rm, mv, find, grep ...
               These tools can be linked against any library.
    /usr/sbin : system administration utility programs
                They usually require superuser privileges to run.
    /usr/local/bin : local additions to the binary utilities
                       Typically these are compiled when installing software locally.