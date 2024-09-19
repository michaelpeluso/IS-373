# Virtualization
*[↑ Previous Article](./README.md)*

## What is Local Virtualization?

Local virtualization is a technology that allows a single physical computer to host multiple virtual machines (VMs), each running its own operating system (OS). This capability is foundational for modern computing, enabling efficient resource utilization and providing a versatile environment for experimentation and learning.

![Illustration of Virtualization Concept](https://www.cloud4u.com/upload/medialibrary/e69/what-is-a-virtualization-techology.png)
*An illustration showing the abstraction layer of virtualization, depicting multiple virtual machines sharing a single physical server.*

### The Concept of Virtualization ## 

Virtualization uses software to create an abstraction layer over physical hardware. This abstraction allows the division of a single computer's hardware components—such as the CPU, memory, and storage—into multiple virtual environments. Each virtual machine operates independently, with its own OS and applications, even though it shares the underlying physical resources with other VMs.

![Diagram of Virtual Machines](https://webimages.mongodb.com/_com_assets/cms/lh54s33za1fuqrg98-VM.jpg?auto=format%252Ccompress)  
*A diagram showing multiple virtual machines running on a single physical server, with each VM having its own OS and applications.*

By leveraging virtualization, you can run multiple operating systems and applications on a single physical machine, optimizing hardware usage and reducing costs. This makes it an essential technology for both personal learning environments and enterprise IT infrastructure.

### Benefits of Virtualization

Virtualization provides several significant advantages:

1. **Resource Efficiency**

   Traditional computing often required dedicating an entire physical server to a single application or operating system. This approach led to underutilized hardware resources. Virtualization allows multiple applications or operating systems to run on the same physical server by creating isolated virtual machines. This improves hardware utilization and reduces costs associated with maintaining multiple physical servers.

   ![Before and After Virtualization](https://github.com/user-attachments/assets/ecfa7881-292a-4696-adc0-fe6707caf90e)
   *Comparison image showing a single server dedicated to one application versus multiple VMs running on the same server after virtualization.*

2. **Simplified Management**

   Virtualization enables centralized management through software-defined VMs. IT administrators can automate tasks such as deployment and configuration using virtualization management tools. This reduces the complexity and time associated with manual setup, making it easier to maintain consistent and repeatable environments.

   ![Virtualization Management Dashboard](https://access.redhat.com/webassets/avalon/d/Red_Hat_Virtualization-4.4-Administration_Guide-en-US/images/08b990f77ee83e09981cedd150d8347d/RHVdashboard.png)  
   *Screenshot of a virtualization management dashboard showing automated deployment and configuration of VMs.*

3. **Reduced Downtime**

   Virtualization supports high availability and disaster recovery by allowing redundant virtual machines to run alongside each other. If a VM encounters issues, administrators can quickly switch to a backup VM, minimizing downtime and maintaining service continuity.

   ![High Availability and Redundancy](https://github.com/user-attachments/assets/2e7d65f0-f39a-4c41-9f04-139076991e0a)
   *Diagram illustrating the concept of high availability with redundant VMs ensuring continuous operation.*

4. **Accelerated Provisioning**

   Setting up new servers traditionally involves purchasing, installing, and configuring physical hardware, which can be time-consuming. Virtualization speeds up this process by allowing administrators to rapidly provision new virtual machines, often through automated scripts or management software.

   ![Provisioning New VMs](https://www.redhat.com/architect/sites/default/files/styles/embed_large/public/2021-09/twostep1.png?itok=6Xep_ekR)  
   *Illustration or screenshot showing the rapid provisioning of virtual machines using automation tools.*

### Virtualization in Practice

Virtualization is widely used across various domains, from personal desktop environments to large-scale data centers. It forms the backbone of cloud computing, where it enables cloud providers to offer scalable and flexible computing resources. Cloud services leverage virtualization to deliver Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS), allowing users to access computing resources and applications on demand.

#### Key Components

- **Virtual Machines (VMs)**: Virtual environments that simulate physical computers. Each VM operates with its own OS and applications, isolated from other VMs.

  ![Virtual Machine Configuration](https://cdn.ttgtmedia.com/digitalguide/images/Misc/anatomy_avm_1.jpg)  
  *Diagram or screenshot showing the configuration and components of a virtual machine.*

- **Hypervisors**: Software layers that manage and allocate hardware resources to VMs. There are two types of hypervisors:
  - **Type 1 (Bare-metal)**: Runs directly on the physical hardware, replacing the traditional OS.
  - **Type 2 (Hosted)**: Runs on top of an existing OS, managing VMs as applications within that OS.

  ![Type 1 vs. Type 2 Hypervisors](https://i.sstatic.net/TAMdL.png)  
  *Illustration comparing Type 1 and Type 2 hypervisors, showing their different architectures and use cases.*

### Getting Started with Virtualization

For individuals and organizations interested in learning about or implementing virtualization, there are various tools and platforms available. This guide provides detailed instructions for setting up local virtualization environments on different operating systems, including Linux, macOS, and Windows. By following these instructions, you can begin exploring virtualization’s potential and apply it to your own projects or infrastructure.

Explore the following sections for in-depth tutorials and resources on how to get started with virtualization on your chosen platform.


### Local Virtualization: A Hands-On Guide to Running Your Own Server

Local virtualization allows you to create and manage virtual machines (VMs) on your computer, enabling you to run different operating systems and experiment with server configurations without affecting your main system. This guide will walk you through setting up local virtualization on Linux, macOS, and Windows.

### Virtualization on Linux

**Linux** provides robust virtualization options. Here’s a guide to using VirtualBox and KVM.

##### **VirtualBox**

1. **Install VirtualBox**

   For Debian-based distributions (e.g., Ubuntu):
   ```bash
   sudo apt update
   sudo apt install virtualbox
   ```

   For Red Hat-based distributions (e.g., Fedora):
   ```bash
   sudo dnf install VirtualBox
   ```

   [Download VirtualBox](https://www.virtualbox.org/wiki/Downloads)

2. **Create a New VM**

   Open VirtualBox and click “New”. Follow the prompts to choose the OS type, allocate memory, and create a virtual hard disk.

3. **Install an Operating System**

   Insert the OS installation media (ISO file) and start the VM. Follow the OS installation instructions.

##### **KVM and QEMU**

1. **Install KVM and QEMU**

   For Debian-based distributions:
   ```bash
   sudo apt update
   sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils
   ```

   For Red Hat-based distributions:
   ```bash
   sudo dnf install @virtualization
   ```

2. **Verify Installation**

   Check if KVM modules are loaded:
   ```bash
   sudo lsmod | grep kvm
   ```

3. **Create and Manage VMs**

   Use `virt-manager` (Virtual Machine Manager) for a graphical interface or `virsh` for command-line management.

   Start `virt-manager`:
   ```bash
   sudo virt-manager
   ```

   To create a VM using `virt-install`:
   ```bash
   sudo virt-install --name myvm --ram 2048 --disk path=/var/lib/libvirt/images/myvm.img,size=20 --vcpus 2 --os-type linux --os-variant ubuntu20.04 --network network=default --graphics spice --cdrom /path/to/ubuntu.iso
   ```

   [Learn more about KVM and QEMU](https://www.linux-kvm.org/)

#### Virtualization on macOS

**macOS** users can use Parallels Desktop, VMware Fusion, or VirtualBox. Here’s a guide for VirtualBox, which is free and open-source.

##### **VirtualBox**

1. **Install VirtualBox**

   Download and install from [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

2. **Create a New VM**

   Open VirtualBox and click “New”. Follow the prompts to set up your VM, selecting the appropriate OS type and allocating resources.

3. **Install an Operating System**

   Insert the OS installation media (ISO file) and start the VM. Complete the installation as you would on a physical machine.

##### **Parallels Desktop and VMware Fusion**

- **Parallels Desktop**: [Download Parallels Desktop](https://www.parallels.com/products/desktop/)
- **VMware Fusion**: [Download VMware Fusion](https://www.vmware.com/products/fusion.html)

Both tools offer user-friendly interfaces for creating and managing VMs.

#### Virtualization on Windows

**Windows** users can use Hyper-V, VirtualBox, or VMware Workstation. Here’s how to use Hyper-V and VirtualBox.

##### **Hyper-V**

1. **Enable Hyper-V**

   Open PowerShell as an Administrator and run:
   ```powershell
   Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
   ```

   Restart your computer when prompted.

2. **Create a New VM**

   Open Hyper-V Manager. Click “New” > “Virtual Machine” and follow the wizard to configure your VM.

3. **Install an Operating System**

   Attach the OS installation media and start the VM to begin installation.

##### **VirtualBox**

1. **Install VirtualBox**

   Download and install from [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

2. **Create a New VM**

   Open VirtualBox and click “New”. Follow the wizard to configure your VM, including selecting the OS  and setting resources.

3. **Install an Operating System**

   Attach the OS installation media (ISO file) and start the VM to begin installation.

##### **VMware Workstation**

- **Download VMware Workstation**: [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html) (free for non-commercial use)

   Follow the installation and VM creation process similar to VirtualBox and Hyper-V.
