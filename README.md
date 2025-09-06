<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://youtu.be/3ZM86XnAXdU)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

## Step 1: Overview

**Configure and install Active Directory services on the designated Domain Controller virtual machine.**

1. Install "Active Directory Domain Services" in DC-1  
   - In the Server Manager dashboard  
   - Click **Add roles and features**  
   - Select **Active Directory Domain Services** and finish the installation.  

<img width="798" height="476" alt="Screenshot 2025-09-06 103735" src="https://github.com/user-attachments/assets/5ddd1d7c-f977-4bc9-985c-9a4ff390cfd8"/>


<p>

## Step 2: Promote DC-1 to Domain Controller

**Configure and install Active Directory services on the designated Domain Controller virtual machine.**

1. Install "Active Directory Domain Services" in DC-1  
   - In the Server Manager dashboard  
   - Click **Add roles and features**  
   - Select **Active Directory Domain Services** and finish the installation.  

<img width="798" height="476" alt="Screenshot 2025-09-06 103735" src="https://github.com/user-attachments/assets/5ddd1d7c-f977-4bc9-985c-9a4ff390cfd8"/>


<p>
