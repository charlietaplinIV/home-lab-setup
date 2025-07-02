# 🧪 Home Lab Setup: Virtual Domain with Windows Server

## 📖 Overview
This lab simulates a small enterprise IT environment using virtualization tools to configure a domain with core Windows Server services such as Active Directory, DNS, and DHCP.

## 🧰 Tools & Technologies
- **Operating Systems**:
  - Windows Server 2022 (Domain Controller)
  - Windows 10 Pro (Client)
- **Roles & Services**:
  - Active Directory Domain Services (AD DS)
  - DNS Server
  - DHCP Server
  - Group Policy Management
- **Networking**:
  - Internal Network Adapter (VirtualBox)
  - Static IP Configuration
- **Utilities**:
  - Remote Desktop Connection
  - Windows Admin Tools


## 🖥️ Lab Environment
- **Host Machine**: [OS, CPU, RAM]
- **VMs**: 1 Domain Controller, 1 Client
- **Network Mode**: [Internal / NAT / Bridged]

## ⚙️ Configuration Steps
1. Installed Windows Server and promoted it to Domain Controller.
2. Configured Active Directory Domain Services.
3. Set up DNS and DHCP Server roles.
4. Created Organizational Units (OUs), users, and groups.
5. Applied Group Policies to control client behavior.
6. Joined client machine to domain.

## 🎯 Skills Demonstrated
- Virtual machine and network setup
- Domain administration and user management
- DNS/DHCP setup and troubleshooting
- Applying and testing Group Policy Objects

## 🧠 What I Learned
- How to resolve domain login failures
- Importance of sequencing network role setups
- Efficient documentation for IT procedures

## 🌱 Future Plans
- Add File Server role and configure NTFS permissions
- Simulate password policies and logon scripts

- ## 📘 Detailed Walkthrough

For a complete guide with screenshots and expanded explanations, check out the [Step-by-Step Walkthrough](walkthrough.md).

- ---
