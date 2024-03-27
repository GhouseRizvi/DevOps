What iss Virtualization??
One computer does job of multiple computer.
one computer runs multiple os parallely

Life before Virtualization:
- We had to buy separate hardware for each OS (Windows, Linux, Mac)
- Each OS was installed on a different hard drive and ran in its own environment
- Users could not use the same resources at  the same time - they were isolated from one another
# To Run App/Service we need servers
# Physiscal Computer (Server in Datacenter)
# One Service - One Server (Isolation)
# Servers are over Provisioned
# Server resource are under utilized
# Huge Cap Ex & Op Ex

Virtual Machine vs Physical Machine
VM is an abstraction layer between the physical.
It allows you to run a guest OS on.
A VM has its own memory, CPU and.
disk storage separate from the host machine.
Types of virtualisation:
1. Monolithic(Layered ): All resources share one interface.
   Example : VMWare Workstation , Parallels Desktop
2. PARAVIRTUALIZATION : Each application sees only part of the hardware .
   Example : Citrix XenServer
3. FULL VIRTUALISATION : Every application sees the full hardware as if it was installed directly on the bare metal.
3. FULL VIRTUALISATION : Every application sees the full hardware as if it was installed directly onto the bare metal. 
3. FULL VIRTUALISATION : Every component of the system is virtualised including the BIOS.
   Example : Microsoft Hyper-V Server / Windows Server 2008 R2 Hyper V
                    VMware ESXi Server / VMware vSphere
                     Oracle Enterprise Linux Virtual Box
                     
Benefits of Virtualisation:
1. Resource Utilisation : Servers can be provisioned with more power than they actually require.
                            This leads to significant cost savings as idle capacity is not used.
2. Application Isolation : If something goes wrong with one application it will not affect others running on the same server.

2. Paravirtualised
3. PV+EPT (Extended Page Tables)
4. Hardware Assisted Virtualisation (HAV)
5. Full System Emulation (FSE)
6. Operating system level virtualisation (OS-level Virt.)
7. Application Level Virtualisation (App-Level Virt.)
8. User Mode HAL (User- Mode Host Abstraction Layer).
9. Virtual PC / Windows XP mode.
It's like running another copy of windows but with access to resources of the main OS.

Advantages of Virtualisation:
1. Cost reduction – You can use cheaper hardware as your server will be using lesser power and space.
2. Flexibility – With virtualisation, you can easily add or remove resources without having to completely rebuild the server. This means that
2. Flexibility – With virtualisation, you can easily add or remove resources as per requirement. This means that if your business grows,
2. Flexibility – With virtualisation, you can easily add or remove resources without having to replace entire machines. This means that if one
2. Flexibility – With virtualisation, you can easily add or remove capacity by simply adding or removing machines within a pool. This means
2. Flexibility – With virtualisation, you can easily add or remove resources as per requirements without any downtime. This means that
2. Flexibility – With virtualisation, you can easily add or remove resources without having to purchase new hardware. This makes it easier for 
2. Flexibility – With Virtualisation, you can easily create new environments by cloning existing ones or creating entirely new machines. This means
2. Flexibility – With virtualisation, you can easily add or remove capacity when needed without having to purchase new hardware. This makes it
2. Flexibility – With virtualisation, you can easily add or remove capacity when needed.

# Terminologies
1. HOST OS
2. Guest OS
3. VM
4. Snapshot
5. Hypervisor

# Types of Hypervisor
# Type 1 Hypervisor
1. Bare Metal
    A hypervisor that manages all aspects of the physical hardware. It starts up everything by  itself and provides a platform for operating systems to boot up.
    - Run as a Base OS 
    - No additional software required
    - High performance
    -  Requires hardware support for virtualization
    - Production
    - Ex VMware esxi, Xen Hypervisor
2. Type 2 Hypervisor
    - Run as Software
    -  Need a special driver in the base OS
    - Lower Performance
    - Does not require hardware support for virtualization
    - Development/Testing Environment
    - Ex Microsoft Hyper-V, Oracle VirtualBox

# Features of Hypervisors
1. Memory Management
   - Dynamic memory allocation
   - Shared memory between multiple VMs
2. Processor Time Sharing
   - Allow multiple VMs to run on  a single physical CPU
3. I/O Virtualization
   - Provide abstractions for devices such as hard drives, network cards etc.
4. Networking Stack
   - Allows each VM to have its own networking stack
5. Paravirtualization
   - Allows VMs to provide services to the host OS without requiring full emulation
6. Live Migration
   - Move running VM from one machine to another while keeping it up and running
7. Resource Reservation
   - Reserve resources (CPU, RAM) for a VM before it starts so that they are guaranteed to be available when needed 
   - Reserve resources (CPU, RAM) for a VM before it starts so that other VMs can use them when needed 
8. Virtulization of Hardware Applications
   - Emulate hardware functions that are not available or do not work properly in a guest operating system
9. Console Redirection
   - Connect a console to a VM instead of a physical device

# Benefits of using a hypervisor
1. Flexibility & Scalability
   - Can run different types of VMs on the same hardware
   - Supports both 32 bit and 64 bit guests
2. Isolation
   - Prevents one VM from affecting another
   - Enables testing new applications or configurations safely
3. Cost savings
   - Runs VMs within a "guest" environment which is isolated from the underlying hardware 
   - Only need enough hardware to run one VM at a time 


