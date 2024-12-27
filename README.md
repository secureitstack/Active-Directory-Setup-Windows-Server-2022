# Setup Active Directory on Windows Server 2022 in Hyper-V

Welcome to the **SecureITStack** guide on setting up **Active Directory** on **Windows Server 2022** using **Hyper-V**! This tutorial is perfect for beginners and walks you through all the essential steps.

---

## 📹 YouTube Tutorial

For a step-by-step video guide, check out the tutorial on our YouTube channel:  
[**SecureITStack - Setup Active Directory on Windows Server 2022**](https://www.youtube.com/c/secureitstack)

---

## 🛠️ Prerequisites

Before starting, ensure that you have the following:
- **Windows 11 Pro** or **Enterprise** with Hyper-V enabled.
- **Windows Server 2022 ISO** for installation.
- A **minimum of 4GB RAM** and **60GB hard drive** for the VM.

---

## ⚙️ Steps to Set Up Active Directory

### Step 1: Enable Hyper-V on Windows 11
- **Windows Features**:  
  Go to **Control Panel > Turn Windows features on or off**, and check **Hyper-V**.
- **PowerShell Alternative**:  
  Run the following command:
  ```powershell
  dism.exe /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V /LimitAccess /All

### ⚙️ Step 2: Create a Virtual Machine
- **Open Hyper-V Manager and follow these steps**:
  1. Click New > Virtual Machine.
  2. Assign a name (e.g., **AD-Server-2022**).
  3. Select **Generation 2**.
  4. Allocate at least **4GB** RAM.
  5. Attach the Windows Server 2022 ISO.
  6. Configure the virtual network switch for connectivity.

### ⚙️ Step 3: Install Windows Server 2022
  1. Boot the VM from the ISO.
  2. Follow the setup wizard and choose the appropriate Windows Server 2022 edition.
  3. Partition the virtual disk and proceed with the installation.
  4. Set an Administrator password after the installation completes.

### ⚙️ Step 4: Promote the VM to Domain Controller
Open Server Manager and select Add roles and features.
Install the Active Directory Domain Services (AD DS) role.
Promote the server to a Domain Controller:
Choose Add a new forest.
Enter the root domain name (e.g., example.local).
Configure DNS and functional levels.
Set a Directory Services Restore Mode (DSRM) password.
Restart the server to complete the process.

📝 GitLab Repository
Access all the automation scripts and detailed documentation in our GitLab repository:
Setup Active Directory Scripts

Scripts include:

Enable Hyper-V via PowerShell.
Automated VM creation using Hyper-V PowerShell modules.
Active Directory promotion script.
🔗 Related Links
SecureITStack YouTube Channel: Visit Channel
Microsoft Docs: Active Directory Basics: Learn More
🚀 Support SecureITStack
If you found this guide helpful, please:

⭐ Star this repository to support the project.
👍 Like and Subscribe to our YouTube channel for weekly tutorials on:
Windows Server
Active Directory
IT Security solutions
Thank you for supporting SecureITStack – Your go-to channel for IT security and server management tutorials!

📌 Keywords for SEO
Active Directory, Windows Server 2022, Hyper-V Setup, Domain Controller, Windows Server Tutorials, SecureITStack, IT Security, Server Management, Tech Tutorials, Windows 11 Hyper-V, Active Directory Setup.
   
