What is linux:
Linux is an open-source operating system that’s similar to Unix. It’s built upon the Linux Kernel, which is the core part that manages how the computer interacts with its hardware and resources. Here’s a brief overview:

1. Linux Kernel: The brain of the OS, ensuring smooth and efficient operation of the system with the hardware.
2. Linux Distributions: Full-fledged operating systems created by combining the Linux Kernel with a collection of software packages and utilities. Popular distributions include Ubuntu, Fedora, and Debian.
3. Open Source: Linux is free to use, modify, and distribute. Its source code is openly available, encouraging collaboration and improvement from developers worldwide.
4. Versatility: Linux is used in a wide range of devices, from personal computers to smartphones and supercomputers.
5. Community: A large and active community supports Linux, contributing to its development and offering support to users

Linux Principles:
1. Linux is an open-source operating system that was developed by Linus Torvalds in 1991. It is based on the Unix operating system and has a kernel designed
1. Open Source - Free to use, modify and distribute. 
2. Portable - Works on multiple hardware platforms with minimal configuration changes.
3. Cross-Platform Compatibility - Runs the same codebase across different operating systems (e.g., Linux, Windows, Mac)

# Everything is a file (including Hardware)
# Small Single purpose Programs
# Ability to chain programs together for complex operation
# Avoid Captive user interface 
# Configuration data stored in text file

Why Linux?
- Cost
- Performance
- Security
- Community Support

What are the differences between Windows & Linux?
- Graphical User Interface vs Command Line Interface
- File System Structure
- Process Management
- Networking Stack

Command Line Interface vs GUI
- Text based input/output
- No mouse or graphic display
- Typically run from terminal window
- Commands entered via keyboard
- Output displayed on screen

File System Structure
- Filesystem Hierarchy Standard (FHS)
    / : Root Directory
        bin : Essential command executables 
        etc : system config files
        lib : libraries
        lost+found : Used by fsck when it finds errors
        opt : Optional packages
        sbin : Superuser command executables
        sys : Kernel and driver software
        usr : User installed applications
            games : Games
            include : C header files
            lib64 : 64 bit libraries
            local : Per-user information
                share : Shared documentation, manual pages, and support files
                    mime : MIME type database
            src : Source code for packages
    
How to navigate directories using Terminal:
cd [directory name]
ls -l : Lists contents of directory with details including permissions.
pwd : Prints current working directory. 
mkdir [directory name] : Creates a new directory.
rm -rf [directory name] : Removes a directory recursively (-f forces removal without prompting).
touch [file name] : Creates a new file.
cat > [filename] <<EOF : Writes text into a file. End with EOF.
chmod +x [filename] : Gives executable permission to the user who owns the file.
cp [source] [destination] : Copies source file to destination. If destination is a directory, copies to that directory.
cp [source filename] [destination filename] : Copies source file to destination file. If no destination is given then it will be copied in

# Architecture of Linux :
The architecture of Linux is a layered structure that comprises several components, each with a specific function. Here’s a simplified overview:

1. Kernel: The core section of the operating system, responsible for managing the system’s resources and communication between hardware and software applications.
2. System Library: Libraries that contain code that the kernel can use to perform different operations. These are useful for accessing the features of the kernel without requiring the application’s code to do all the work.
3. Hardware Layer: This includes all the physical devices that make up the system, such as the CPU, memory, disk drives, etc.
4. System Utility: Programs that perform individual, specialized management tasks.
5. Shell: A command-line interface that allows users to interact with the operating system by entering commands.

+------------------+
|      Shell       |
+------------------+
|   System Utility |
+------------------+
|   System Library |
+------------------+
|      Kernel      |
+------------------+
|     Hardware     |
+------------------+

The kernel is responsible for managing hardware resources such as memory, disks, network interfaces etc. It provides services to system utility programs which in
The kernel is responsible for hardware interaction, memory allocation, process scheduling, I/O handling etc. 
System utility programs interact directly with the system library which  in turn communicates with the kernel.


Linux Distros:
Linux distributions, commonly known as “distros,” are various flavors of Linux, each tailored to meet specific needs or preferences. They bundle the Linux kernel with a set of software to provide a complete operating system. Here are some categories and examples of Linux distros:

For General Use:
1. Ubuntu: Known for its user-friendliness and wide support.
2. Fedora: Features cutting-edge technology and innovation.
3. Debian: Praised for its stability and reliability.
For Beginners:
4. Linux Mint: Offers a familiar environment for those transitioning from Windows.
5. elementary OS: Focuses on a clean and simple user experience.
For Advanced Users:
6. Arch Linux: A rolling release system that is highly customizable.
7. Gentoo: Known for its optimizations and fine-grain control.
For Specific Purposes:
8. Kali Linux: Designed for penetration testing and security auditing.
9. Tails: Aimed at preserving privacy and anonymity.
Lightweight:
10. Lubuntu: A lightweight version of Ubuntu, great for older hardware.
11. Puppy Linux: Extremely small and runs entirely in RAM.
For Servers:
12. CentOS: Free enterprise-class computing platform.
Ubuntu Server: Offers stability and support for server applications.
Specialized Ubuntu-Based Distros:
13. Kubuntu: Ubuntu with the KDE desktop environment.
14. Xubuntu: Ubuntu with the Xfce desktop environment.
15. Ubuntu Budgie: Ubuntu with the Budgie desktop environment1.
Each distro has its own community and ecosystem, making Linux a diverse and flexible operating system choice. 
