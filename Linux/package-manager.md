what is package manager in linux ?

A package manager in Linux is a set of software or tools that allows users to effectively manage software packages. These package managers handle tasks such as installing, upgrading, removing, and configuring packages on the Linux operating system. Let’s dive into the core concepts surrounding Linux package management:

Packages:
A package is at the heart of the Linux operating system. It’s an archive file containing:
An executable binary file: The actual software or application.
A related configuration file: Settings and preferences for the software.
Information about dependencies: Other packages required for the software to function correctly.
Think of a package as any software or application that can run on Linux, whether it’s a command-line tool or a GUI application.
Packages can also act as dependencies for other software programs to run.
Dependencies:
The Linux operating system is complex, consisting of multiple software components that depend on each other.
When you install a package, it often relies on other packages to function properly.
For example, an application might utilize open-source libraries (dependencies) rather than reinventing the wheel by developing everything from scratch.
Package managers handle these dependencies automatically, ensuring that all required software components are available.
Pre-compiled Packages:
In the past, software needed to be manually compiled from source code.
Users had to find dependencies, download them, and install them manually.
This process was tedious and error-prone.
Linux introduced its package management system to simplify software management.
Packages are pre-compiled, meaning the package manager doesn’t have to compile the source code; it directly installs the pre-built package.


Yum
