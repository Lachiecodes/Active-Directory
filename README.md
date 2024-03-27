# Building an Enterprise Active Directory Environment


## Introduction
In today's digital landscape, establishing a robust network infrastructure is essential for organizations to ensure seamless operations and effective resource management. One critical component of such infrastructure is an Active Directory (AD) environment, which provides centralized authentication, authorization, and network management capabilities. 

In this lab I used two virtual machines on VirtualBox to simulate an Active Directory environment using Windows Server 2019, and Windows 10. After configuring IP Addressing, DNS, AD/DS, NAT/RAS, and DHCP, I use a PowerShell script to create 1000 users in Active Directory. Finally, we create a client machine on Windows 10 to connect to the virtual network and add it to Active Directory.

## Selecting the Virtualization Software
Choosing the right virtualization software is the first step in creating a virtualized environment for Windows Active Directory. While I utilized Oracle VM Virtualbox, any virtualization software such as Hyper-V or VMware can be used. The key is to ensure compatibility with your system and the ability to run multiple virtual machines (VMs) concurrently.

## Creating Virtual Machines


## Overview of Virtual Machines


## Explanation of the Configuration


## Conclusion
Setting up a Windows Active Directory environment is a meticulous process that requires careful planning and execution. By leveraging virtualization technology and following best practices in configuration and policy settings, organizations can establish a robust foundation for their IT infrastructure.

It's important to note that specific configurations may vary based on software versions, network requirements, and security policies. Always refer to official documentation and consult with IT professionals when implementing complex network architectures. With proper implementation, an efficient and secure AD environment can be tailored to meet the unique needs of any organization.
