<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Deploying Active Directory</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create a Domain Admin User within the Domain
- Join Client-1 to your domain
- Setup Remote Desktop for non-administrative users on Client-1
- Create a bunch of additional users and attempt to log into client-1 with one of the users

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/6QstXgn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Created an three organizational units called _ADMINS, _EMPLOYEES, and _CLIENTS to group admins, employees, and computers logically within the domain. Organizational Units allow admins to apply policies, manage permissions, and streamline security settings. Created an admin user called Jane Doe. A account does not become admin just by being added to the _ADMINS folder. You have to add the user to the built-in domain admins security group to give the account admin rights. 
</p>
<br />

<p>
<img src="https://i.imgur.com/RYJMBHJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Added Client-1 to the domain. From the computers folder in DC-1 we dragged Client-1 into the _CLIENTS folder. 
</p>
<br />

<p>
<img src="https://i.imgur.com/p4I0JT8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In Client-1 changed the remote desktop settings so that anyone who is a Domain User in DC-1 is able to log into the Client-1 computer.
</p>
<br />
