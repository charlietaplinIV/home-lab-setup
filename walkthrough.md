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
On Virtural Box Orcal Manager Start the program and select New to start the creation of your first virtual machine.

- **Name**: DC01 <--- Name this for your own cusmtom domain controller name!
- **OS (ISO Image)**: Windows Server 2022 <--- Locate your Windows Server 2022 ISO and select it.
**Please Be Sure To Select Desktop Experience In The Edition Tab If You Want A Desktop Enviroment!**

![Screenshot 2025-06-30 200324](https://github.com/user-attachments/assets/97748b96-5475-439b-93fe-a341a19f6b84)

- **Username & Password**: Administrator <-- create your own username and password to login to your DC.
- **Hostname**: DC01 <-- Should be the same as the name you typed in on the previeous page.

![Screenshot 2025-06-30 200501](https://github.com/user-attachments/assets/22555490-7682-4f9a-bbbe-00ad4a5b0bca)

- **RAM (Base Memory)**: 2–6 GB <-- recommend 2GB of ram to not use up host computer resources.
- **Processors**: 2
- **Storage**: 40–60 GB (Dynamically allocated)
- **Network Adapter**: Internal Network (create a new one called `LabNet` or similar)

After all settings are done hit finish and let the VM run the windows setup! 

#### VM 2: Client Machine
On Virtural Box Orcal Manager Start the program and select New to start the creation of your Windows 10 Machine.

- **Name**: Win10-PC <--- Name of your Windows 10 PC
- **OS**: Windows 10 Pro <--- Locate your Windows 10 ISO and select it.
- **RAM**: 2–4 GB
- **Processors**: 1–2
- **Storage**: 30–50 GB
- **Network Adapter**: Internal Network (`LabNet`)
- **Troubleshooting Fix** If you are getting "Windows cannot read the <ProductKey> setting from unattend answer file." Follow these steps to fix the error!
- Step 1 - Shutdown your Windows 10 VM
- Step 2 - Open FIle Expolere and head to C:/Users/yourprofile/Virtual VMs/Windows 10 VM Machine Name
- Step 3 - Delete any Unattended files in the directory.
- Step 4 - Close File Explorer and start your Virtural Machine back up.
- Step 5 - Continue Windows 10 Installation! <-- Make sure to choose Windows 10 Pro as your OS System.

---

## 🔐 Step 2: Install & Configure Windows Server 2022

### 🖥️ Post-Installation Configuration
1. Open **Server Manager**.
2. Set a static IP address via:
   - **Network and Sharing Center** → Adapter settings → Ethernet 2 → IPv4 properties.
   - Example:  
     - IP: `192.168.10.10`  
     - Subnet: `255.255.255.0`  
     - Default Gateway: leave blank or `192.168.10.1`  
     - Preferred DNS: `192.168.10.10` (self-reference) <-- You can also use 127.0.0.1 as a loopback address!

![Screenshot 2025-07-01 052442](https://github.com/user-attachments/assets/7a7b9095-d69e-4b78-88cd-959bd109004f)

---

### ⚙️ Promote to Domain Controller
1. In Server Manager,  go to Manage and click **Add Roles and Features**.
3. Click Role Based or Featured Base Installation in the `Installation Type` Tab.
4. In `Server Selecton` choose the domain controller (DC01) in the sever pool.
5. Select **Active Directory Domain Services (AD DS)** in the `Server Roles` Tab.
6. Click next on the rest of the tabs until you get to Confirmation then select Install.
7. After installation, click the yellow flag in Server Manager → **Promote this server to a domain controller**.
8. Choose:
   - **Add a new forest**
   - Domain name: `mydomainname.local`
9. Set a DSRM (Directory Services Restore Mode) password.
10. Accept the defaults for DNS and NetBIOS.
11. Review, install, and reboot.

---

### ✅ Confirmation Steps
- Open **Active Directory Users and Computers** and verify your domain.
- Test local administrator login with domain name (e.g., `charliedomain\Administrator`).
- Check DNS Manager to verify zones were created.

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
