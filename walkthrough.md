# 📝 Step-by-Step Walkthrough: Home Lab Setup

This guide walks you through building a Windows Server 2022 domain environment from scratch using VirtualBox and a Windows 10 Pro client.

## 📦 Tools Needed
- VirtualBox
- ISO for Windows Server 2022 and Windows 10 Pro
- Time and patience! 

---

## 🔧 Step 1: Create Your Virtual Machines
## Step 1: Set Up Your Virtual Environment

### 🧰 Tools Needed:
- [VirtualBox](https://www.virtualbox.org/) (Installed on your host machine)
- ISO files for:
  - <a href="https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022?msockid=00069a2577c2606a3b858ff7769561ac" target="_blank" rel="noopener noreferrer">Windows 2022</a> (Evaluation version available from Microsoft)
  - <a href="https://www.microsoft.com/en-us/software-download/windows10?msockid=00069a2577c2606a3b858ff7769561ac" target="_blank" rel="noopener noreferrer">Windows 10</a>

---

### 🖥️ Create Your Virtual Machines

#### VM 1: Domain Controller
- **Name**: DC1
- **OS**: Windows Server 2022
- **RAM**: 4–6 GB
- **Processors**: 2
- **Storage**: 40–60 GB (Dynamically allocated)
- **Network Adapter**: Internal Network (create a new one called `LabNet` or similar)

#### VM 2: Client Machine
- **Name**: Win10-PC
- **OS**: Windows 10 Pro
- **RAM**: 2–4 GB
- **Processors**: 1–2
- **Storage**: 30–50 GB
- **Network Adapter**: Internal Network (`LabNet`)

## 🔐 Step 2: Install & Configure Windows Server 2022
...

## 🧠 Step 3: Configure Active Directory, DNS, DHCP
...

## 👥 Step 4: Create OUs, Users, Groups
...

## 💻 Step 5: Join Windows 10 Client to Domain
...

## 🧪 Step 6: Test Everything
...

## 🖼️ Screenshots
*Add images here as you go*

---

*Coming soon: [Planned Enhancements]*
