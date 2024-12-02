<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory
- Create a Domain Admin User within the domain
- Join one of your VM's to your domain
- Use your Domain Controller Server to Create additional users

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/90473a96-3565-43d8-b114-4dea049f787d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Login in to your Domain Controller Server in your VM. Click start and go to Active Directory Users and Computers (ADUC). Right click on "my domain.com' and click new. Then click new organizational unit. In this project I titled my users organizational unit as "_CLIENTS". 
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5e7c630e-d2b5-48f5-89d5-35a44eb77f7d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the ADUC, I then created more organizational units. I created an admin under the name of "Jane". Once created. I then logged into my other remote desktop virtual machine and allowed "domain users" access to the remote desktop. 
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/6f341e68-d9e7-4115-a07e-9fbc5427cbc2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On your domain controller virtual machine using Microsoft Azure, Login as an admin created using "mydomain.com\(user_admin)". Any user you chose as an admin will the name you choose instead of "user". Open Powershell_ise, make sure you run as an administrator. Create a new file and paste the contents of this

[SCRIPT](https://docs.google.com/document/d/1flsnrCyBg_lSCP2MB6D5T53G08fhyrONboqYvzkRYg8/edit?usp=sharing)  When finished, open Active Directory Users and Computers (ADUC) and observe the accounts.
</p>
<br />
