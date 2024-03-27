What is Vagrant??
//===============================================
Vagrant is an open-source software for building and managing virtual development environments.  It uses a combination of Docker, NFS, 


Vagrant solve the VM Managment Problems, created manually
1. OS installation
2. Time Consuming
3. Manual chance of human error.
4. Tough to replicate multi vms.
5. Need to document entire setup

Advantages of Vagrant:
- Easy to use and understand 
- Lightweight (VM's are not heavy)
- Portable across different platforms

How does it work?
- You write a file called "Vagrantfile" in your project directory which describes how you want your virtual machine to be configured.
- Virtual Machine Management Tool
- Runs on your machine/OS

- Creates a virtual machine in user space using software like Hypervisor or VirtualBox
- Configures that VM with specific settings such as IP address, hostname etc.
- Provides an interface for managing those configurations through a simple YAML file called "Vagrantfile"

Commands available in Vagrant:
shutdown halt suspend reload restart provision sshconfig status ip addr vm_show help

Let's start by creating our first project:
bash$ mkdir myproject && cd myproject
myproject$ vagrant init ubuntu/trusty64
This will create a new folder named 'myproject' containing a file named 'Vagrantfile'. This file contains all the configuration needed for our
This will create a new folder named 'myproject' containing a file called 'Vagrantfile'. This file contains all the configuration needed for our Creating vm.

Vagrant Architechture:
1. create a Folder
2. create  a VagrantFile inside that folder
3. run vagrant up command which will do following things:
   - download the base box if not already
   - configure the VM according to VagrantFile
   - launch the VM

Structure of VagrantFile
ruby<<EOF
require 'yaml'
puts <<EOF
# A basic Vagrantfile to get you started with Vagrant
# https://docs.vagrantup.com/v2/getting-started/index.html
#
# Copyright (c) 2015 Vagrant Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License  

