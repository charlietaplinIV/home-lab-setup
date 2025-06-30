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
- **Name**: DC1 <--- Name this to your own cusmtom domain controller name!
- **OS (ISO Image)**: Windows Server 2022 <--- Locate your Windows Server 2022 ISO and select it.
**Please Be Sure To Select Desktop Experience In The Edition Tab If You Want A Desktop Enviroment!**

![Screenshot 2025-06-30 002436](https://github.com/user-attachments/assets/3c04b0a1-a05d-4496-944d-243446c960b3)
 
- **Username & Password**: charlie4 <-- create your own username and password to login to your DC.
- **Hostname**: DC1 <-- Should be the same as the name you typed in on the previeous page.
- **Domain Name**: charlie4.visuals.org <-- contains the custom domain name you will be using.

![Screenshot 2025-06-29 064019](https://github.com/user-attachments/assets/56ef8338-06fe-4a87-86a8-76d1cf2d37f6)


- **RAM**: 2–6 GB <-- recommend 2GB of ram to not use up host computer resources.
- **Processors**: 2
- **Storage**: 40–60 GB (Dynamically allocated)

After configuring and all settings close and power off your Windows Server VM for now so we can setup the network!

- **Network Adapter**: Internal Network (create a new one called `LabNet` or similar)
- With your Windows Server Selected hit the Settings Icon and Navagiate to Network. Enable your Network Adapter 1 and change the `Attached to` section to Internal Network and name it to your desired Network Name.

![Screenshot 2025-06-30 001227](https://github.com/user-attachments/assets/fcf6aa9a-927a-4cd5-908b-183fa5062edd)

Now run the virtural machine and let it install your Windows Server!
After Windows Server 2022 install is complete shut down the virtural machine and head back to your Settings and navagiate to `Storage`. In the storage settings click on your ISO file you used to install windows and in the `Attributes` section click the CD icon and then click Remove Disk From Virtual Drive. This will help prevent the VM from running the windows installation agian.

![Screenshot 2025-06-30 005201](https://github.com/user-attachments/assets/db35e5e6-17f0-47af-afe3-bc96ccd65e13)


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
