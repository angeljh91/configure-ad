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

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/user-attachments/assets/5572da20-b96c-495e-8d7a-d85d952cd0d9)

First the Domain Controller Virtual Machine (Windows Server 2022) named "DC-1" was created. We then went on to creating the Resource Group and Virtual Network (Vnet). Next we set the Domain Controller's NIC Private IP address to static. Finally, we created the Client Virtual Machine (windows 10) and named it "Client-1." It was created with the same Resource Group and Vnet created in DC-1. The topology was checked with the Network Watcher, to ensure that both Virtual Machines were in the same network.
