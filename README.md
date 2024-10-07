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

![image](https://github.com/user-attachments/assets/bc02c47c-372d-43cb-8cfd-cdc48675085f)

Connectivity between the client and Domain Controller was ensured by logging into Client-1 with Remote Desktop and pinging DC-1’s private IP address with ping -t (perpetual ping). ICMPv4 were enabled on the local windows Firewall. After logging back into Client-1 check to make sure the ping is successful.

![image](https://github.com/user-attachments/assets/ce0f1694-c340-4242-bb3c-a50d67ad9f7b)

This shows a demonstration of me using wizard to install Active Directory. When utilizing wizard checks are done specifically to note whether the server meets the requirements necessary to become a Domain Controller. The wizard checks server roles and features, Configuration, Forest and Domain Functional levels, permissions and Active Directory Database path.

![image](https://github.com/user-attachments/assets/8f24038b-db30-4d5e-8c94-94a80f174585)

Power Shell ISE is a scripting tool provided by Microsoft to write and edit Power Shell scripts. Power Shell enhances the management of Active Directory, making it more efficient, reliable, and scalable. Here we have a demonstration of me creating users in Active Directory Domain Controller using Power Shell ISE.
