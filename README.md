# Building an Active Directory Environment
 ![260781883-9a11fa39-b1ad-432e-a010-465602dce3bf](https://github.com/Lachiecodes/Active-Directory/assets/138475757/aad72280-e6e2-40a1-a7f3-6d3ce19dac06)

## Introduction
In today's digital landscape, establishing a robust network infrastructure is essential for organizations to ensure seamless operations and effective resource management. One critical component of such infrastructure is an Active Directory (AD) environment, which provides centralized authentication, authorization, and network management capabilities. 

For this project, VMware was utilized to create an integrated environment that consisted of a Windows Server 2019 Virtual Machine (VM) serving as the Domain Controller (DC) with Active Directory (AD) service. A custom PowerShell script was then executed to populate AD with approximately 1000 fictional users. I then created a client machine on Windows 10 to which was integrated into the AD domain's internal network.

## Technologies and Components Utilized:
- Active Directory
- AD Domain Service
- NAT
- DNS
- Networking
- PowerShell
- VMware
- Windows Server 2019
- Windows 10

## Windows Server 2019 Setup
- Two network adapters were used to separate traffic between external and internal.
  ![68747470733a2f2f692e696d6775722e636f6d2f5751796478314d6c2e706e67](https://github.com/Lachiecodes/Active-Directory/assets/138475757/1ba37026-0246-4941-85e2-3ec9954c411f)

- The following roles and services were configured.
  ![68747470733a2f2f692e696d6775722e636f6d2f68444a347679666c2e706e67](https://github.com/Lachiecodes/Active-Directory/assets/138475757/73d212ab-940d-48b2-a1c0-f0b0001e559e)

- PowerShell script used to generate approximately 1000 fictional users.
  ![68747470733a2f2f692e696d6775722e636f6d2f64684e495263716c2e706e67](https://github.com/Lachiecodes/Active-Directory/assets/138475757/4d6ed4db-6f2a-4372-8b55-24778f9e0d73)
  ![68747470733a2f2f692e696d6775722e636f6d2f434730507538766c2e706e67](https://github.com/Lachiecodes/Active-Directory/assets/138475757/eb298c63-b9fe-455b-966f-c876d0a39358)

- After the configurations were completed, I then took time to explore AD by performing tasks such as: creating groups, organizational units, modifying user permissions, disabling users, deleting users, and so on.
![68747470733a2f2f692e696d6775722e636f6d2f3246564c6a356d6c2e706e67](https://github.com/Lachiecodes/Active-Directory/assets/138475757/4d06030c-f4d3-47ea-8b1f-ed177f845519)

## Connecting Windows 10 Machine to AD
- The creation of the Windows VM was straightforward and I encounted no issues.
- During the installation I placed the VM on the internal network and created a local account.
- I then updated the system's name and joined it to my domain.<br>
  ![68747470733a2f2f692e696d6775722e636f6d2f3936427a416c696d2e706e67](https://github.com/Lachiecodes/Active-Directory/assets/138475757/22ce57a1-ac13-4477-a610-ffcf895b7bc5)

- From there I verified the VM was connected to AD by logging into several of the random users I had created.
  ![68747470733a2f2f692e696d6775722e636f6d2f546f45363050676d2e706e67](https://github.com/Lachiecodes/Active-Directory/assets/138475757/c082ad84-7199-4d2c-88c9-970f27caf648)

## Conclusion
In this project, VMware was used to create an integrated AD environment. The first VM was a Windows Server 2019 that served as the DC, DHCP, and Active Directory populated with approximately 1000 users. Once the networking configurations were complete for the server, I then created one more VM and connected them to an internal network using Active Directory.

Setting up a Windows Active Directory environment is a process that requires careful planning and execution. By leveraging virtualization technology and following best practices in configuration and policy settings, organizations can establish a robust foundation for their IT infrastructure.

It's important to note that specific configurations may vary based on software versions, network requirements, and security policies. Always refer to official documentation and consult with IT professionals when implementing complex network architectures. With proper implementation, an efficient and secure AD environment can be tailored to meet the unique needs of any organization.
