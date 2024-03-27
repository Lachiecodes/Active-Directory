# Building an Enterprise Active Directory Environment

![1711131630329](https://github.com/Lachiecodes/Active-Directory/assets/138475757/76ded16b-f089-4f78-a96a-9efafe198e9e)
## Introduction
In today's digital landscape, establishing a robust network infrastructure is essential for organizations to ensure seamless operations and effective resource management. One critical component of such infrastructure is an Active Directory (AD) environment, which provides centralized authentication, authorization, and network management capabilities. 

In this lab I used two virtual machines on VirtualBox to simulate an Active Directory environment using Windows Server 2019, and Windows 10. After configuring IP Addressing, DNS, AD/DS, NAT/RAS, and DHCP, I use a PowerShell script to create 1000 users in Active Directory. Finally, we create a client machine on Windows 10 to connect to the virtual network and add it to Active Directory.

## Selecting the Virtualization Software
Choosing the right virtualization software is the first step in creating a virtualized environment for Windows Active Directory. While I utilized Hyper-V due to having Windows 11 Pro, any virtualization software such as VirtualBox or VMware can be used. The key is to ensure compatibility with your system and the ability to run multiple virtual machines (VMs) concurrently.

## Creating Virtual Machines
The initial phase involves creating four essential virtual machines based on the network topology provided in a YouTube video (link to be inserted). Each VM should be configured with at least 2 CPU cores and a minimum of 50GB of SSD space to ensure optimal performance. Organizing ISO images for installations in a structured manner within File Explorer simplifies the setup process and enhances efficiency.

## Overview of Virtual Machines
Hyper-V External Virtual Switch: This connects the virtual environment to the external network, enabling internet access for the VMs.
Hyper-V Internal Virtual Switch: Facilitates internal communication among the VMs, ensuring seamless interaction within the network.

ALD10101 (Windows 10 Client for Testing): This VM serves as a Windows 10 client machine for testing purposes within the AD environment. I mostly test student accounts with this VM.

Domain Controller (Name: Thor): Configured with Network Address Translation (NAT), responsible for creating the domain, managing user accounts, and assigning home folders.
IP Address: 10.0.0.101
Subnet Mask: 255.255.255.0
Gateway: N/A (Not Applicable)
DNS: 127.0.0.1
Domain: acs.edcc.ctc.edu

DHCP Server (Name: Atlas): Manages dynamic IP address allocation within the network, with a defined range and gateway.
IP Address: 10.0.0.102
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.101
DNS: 10.0.0.101

File Server (Name: Zeus): Handles file storage and sharing, maintaining appropriate permissions for domain users.
IP Address: 10.0.0.103
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.101
DNS: 10.0.0.101

## Explanation of the Configuration
The IP addressing and network configuration ensure that each component of the AD environment can communicate effectively and access necessary resources. The use of a consistent subnet (10.0.0.0/24) allows seamless communication between devices without requiring routing between subnets. By leveraging the domain controller (Thor) for DNS services and potentially for routing, the network maintains centralized control and efficient management of network traffic.

Overall, the carefully configured IP addresses, subnet masks, gateways, and DNS settings form the backbone of a functional and interconnected Active Directory environment, enabling secure and efficient operations within the network infrastructure.

## Conclusion
Setting up a Windows Active Directory environment is a meticulous process that requires careful planning and execution. By leveraging virtualization technology and following best practices in configuration and policy settings, organizations can establish a robust foundation for their IT infrastructure.

It's important to note that specific configurations may vary based on software versions, network requirements, and security policies. Always refer to official documentation and consult with IT professionals when implementing complex network architectures. With proper implementation, an efficient and secure AD environment can be tailored to meet the unique needs of any organization.
