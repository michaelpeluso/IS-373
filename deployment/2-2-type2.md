# Virtualization Hypervisors: Type 2
*[↑ Previous Article](./2-0-virtualization.md)*

## Introduction
While Type 1 hypervisors operate directly on hardware, Type 2 hypervisors, also known as **hosted hypervisors**, run atop a conventional operating system. This section explores Type 2 hypervisors, examining their architecture, benefits, drawbacks, and typical applications in various computing environments.

## Architecture
Type 2 hypervisors are installed as software applications on a host operating system (OS). They leverage the host OS to manage hardware resources and facilitate the creation and operation of virtual machines. Each VM runs its own guest OS and applications, relying on the Type 2 hypervisor to mediate access to physical hardware through the host OS.

## Key characteristics of Type 2 hypervisors include:
- **Host OS Dependency**: They require an underlying OS, which handles device drivers, memory management, and other system functions.
- **User-Friendly Interface**: Often designed with user interfaces that make installation and management straightforward, catering to both casual and professional users.
- **Flexibility**: They support a wide range of guest operating systems and are typically easier to set up on existing hardware.

## Advantages
1. **Ease of Use**: Type 2 hypervisors are generally easier to install and configure, making them accessible to users with varying levels of technical expertise.
2. **Cost-Effective**: Many Type 2 hypervisors are free or come at a lower cost compared to their Type 1 counterparts, making them attractive for individual users and small businesses.
3. **Flexibility**: They allow users to run multiple operating systems on their existing hardware without significant changes to their setup.
4. **Convenience for Development and Testing**: Ideal for software developers and testers who need to create and manage multiple environments without dedicated hardware.

## Disadvantages
1. **Performance Overhead**: Running on top of a host OS introduces additional layers that can degrade performance compared to Type 1 hypervisors.
2. **Limited Scalability**: Type 2 hypervisors are not typically designed for large-scale deployments, making them less suitable for enterprise environments.
3. **Security Risks**: The dependence on the host OS can introduce vulnerabilities, as the security of the VMs is partly reliant on the security of the host system.
4. **Resource Contention**: Since the host OS manages hardware resources, VMs may compete for resources, potentially leading to performance bottlenecks.

## Common Use Cases
- **Personal Computing**: Ideal for individuals who need to run multiple operating systems on their personal computers for various tasks such as software testing, gaming, or accessing different applications.
- **Development and Testing**: Developers use Type 2 hypervisors to create isolated environments for testing applications across different operating systems and configurations.
- **Educational Purposes**: Educational institutions utilize Type 2 hypervisors to teach students about different operating systems and virtualization technologies without requiring extensive hardware resources.
- **Small Businesses**: Small enterprises leverage Type 2 hypervisors for cost-effective virtualization solutions, enabling them to maximize their existing hardware investments.

## Popular Type 2 Hypervisors
- **VMware Workstation and VMware Fusion**: Widely used for professional development and testing, offering robust features and integration with VMware’s ecosystem.
- **Oracle VM VirtualBox**: An open-source hypervisor favored for its versatility and support across multiple host and guest operating systems.
- **Microsoft Virtual PC and Hyper-V (hosted mode)**: Provide virtualization solutions integrated with Windows environments, suitable for both casual and professional use.
- **Parallels Desktop**: Popular among Mac users for running Windows and other operating systems seamlessly alongside macOS.

## Performance Considerations
While Type 2 hypervisors offer significant flexibility and ease of use, their performance is inherently limited by the additional overhead of the host OS. Resource-intensive applications may experience reduced performance compared to running on a Type 1 hypervisor or directly on physical hardware. However, advancements in virtualization technology and hardware acceleration features have mitigated some of these performance impacts, making Type 2 hypervisors more viable for a broader range of applications.

## Security Implications
The security of VMs under a Type 2 hypervisor is closely tied to the security of the host OS. Vulnerabilities in the host can potentially compromise all running VMs. Therefore, maintaining a secure and updated host environment is crucial when using Type 2 hypervisors. Additionally, users should implement best practices such as isolating sensitive VMs and using strong authentication mechanisms to enhance security.

## Conclusion
Type 2 hypervisors offer a flexible and cost-effective virtualization solution, particularly suited for personal use, development, testing, and small business applications. Their ease of installation and management, combined with broad OS support, make them an attractive choice for users seeking to run multiple operating systems on a single physical machine. However, considerations regarding performance overhead, scalability, and security must be addressed to ensure optimal and secure operation. As virtualization technology continues to evolve, Type 2 hypervisors remain a valuable tool in the diverse landscape of computing environments.
