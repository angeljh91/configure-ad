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

<p>
<img src="https://i.imgur.com/gRvLkd5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In step 1, the Resources in Azure were setup. The Domain Controller VM (Windows Server 2022) named “DC-1” was created while simultaneously creating the Resource Group and Virtual Network (Vnet). The Domain Controller’s NIC Private IP address was set to static. The Client VM (Windows 10) named “Client-1” was created with the same Resource Group and Vnet that was created in DC-1. The topology was checked with the Network Watcher, to ensure both VM's were in the same network. 


</p>
<br /> 

<p>
<img src="https://i.imgur.com/vCZMGfK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In step 2, Connectivity between the client and Domain Controller was ensured by logging into Client-1 with Remote Desktop and pinging DC-1’s private IP address with ping -t <ip address> (perpetual ping). ICMPv4 were enabled on the local windows Firewall. After logging back into Client-1 check to make sure the ping is successful. 

 

</p>
<br />

<p>
<img src="https://i.imgur.com/7g0Byol.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In step 3, Active Directory Domain Services was Installed by logging in to DC-1. Promoted as a DC: a new forest as mydomain.com was setup. Remote Desktop was Restarted and logged back into DC-1 as user: mydomain.com\labuser.
</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/GbbLxQW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In step 4, Remote Desktop was setup for non-administrative users jane_admin was used a the user name,
PowerShell_ise was opened as an administrator. A new File was created and pasted into the contents of the script. When the script is run, account will created. The accounts can now be viewed in Active Directory in the appropriate organizational unit.

  
</p>
<br />
