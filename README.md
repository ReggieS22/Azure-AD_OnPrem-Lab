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


2. Click on the flag at the top right of the screen with the warning sign  
   - Promote DC-1 to Domain Controller
   - Setup a new foret as "mydomain.com"
   - Restart and then log back into DC-1 as user: mydomain.com\reggie-admin  

<img width="798" height="476" alt="Screenshot 2025-09-06 103802" src="https://github.com/user-attachments/assets/f0458eed-f2c0-4039-9548-0e1325a9222b"/>





- Run Active Directory Users & Computers shown below.



<img width="822" height="494" alt="Screenshot 2025-09-06 103819" src="https://github.com/user-attachments/assets/dbf5c75f-b67e-4df0-8c55-8a2472d6abc3"/>
<p>







## Step 3: Create an Organizational Unit(OU) named _EMPLOYEES and _ADMINS

   - Right click on mydomain.com and select New and click on Organizational Unit
<img width="827" height="494" alt="Screenshot 2025-09-06 103839" src="https://github.com/user-attachments/assets/06054437-fc5b-4bcc-aa85-9310cd0ec976"/>


- Create OU_EMPLOYEES and _ADMINS

<img width="828" height="494" alt="Screenshot 2025-09-06 103851" src="https://github.com/user-attachments/assets/bb94dd8e-eb7e-4700-afc7-bd608abc2407"/>
<p>




## Step 4: Create a Domain Admin user within the domain


   - Right click on the OU  _ADMINS and create a new user named Jane Doe.
   - With the username jane_admin  

<img width="827" height="497" alt="Screenshot 2025-09-06 103920" src="https://github.com/user-attachments/assets/52be3374-5a35-4afd-823c-65ad6d7f6e34" />
<p>




## Step 5: Add jane_admin to the "Domain Admins" Security Group 


   - Turn Jane Doe into an admin by right clicking her name > properties
   - member of and adding her to the "Domain Admins" Security Group

<img width="829" height="495" alt="Screenshot 2025-09-06 104037" src="https://github.com/user-attachments/assets/e911f82c-4922-49ea-a400-afaf42c1e959" />

<p>


## Step 6: Log out of DC-1 to log back in as Jane Doe


   - Log back in as "mydomain.com\jane_admin"
   - Use jane_admin as your admin account from now on

<img width="453" height="557" alt="Screenshot 2025-09-06 104858" src="https://github.com/user-attachments/assets/a2406d9b-e020-47ef-8727-cc6a44ddbd49" />


<p>



