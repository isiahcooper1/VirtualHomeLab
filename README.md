<h1>Virtual Home Lab</h1>

<h2>Description</h2>
This project demonstrates the deployment of a small-scale on-premises Active Directory environment in a mixed Windows and Linux network. This lab simulates a typical SMB infrastructure and focuses on core system administration services: identity management, name resolution, IP address management, and centralized file sharing. <br>
<br />
This environment was built entirely using virtual machines and is designed to mirror how these foundational services are commonly implemented in real-world enterprise networks.
<br />


<h2>Utilities Used</h2>

- <b>Hyper-V</b> 
- <b>Active Directory Domain Services (AD DS)</b>
- <b>DNS Server</b>
- <b>DHCP Server</b>
- <b>SMB / NTFS</b>
- <b>PowerShell</b>
- <b>realmd /SSSD</b>

<h2>Environments Used </h2>

- <b>Windows Server 2022</b>
- <b>Windows 11</b> (21H2)
- <b>Ubuntu Server</b>
- <b>Isolated Virtual Network</b>

<h2>Walk-through:</h2>

<p align="center">
Launched 3 VMs in Hyper-V - One UI-based domain controller, one server core domain controller, and one file server. Installed Windows Server 2022 on all 3 servers. Created an external virtual switch and configured all 3 VMs to use the same switch. Configured all 3 servers to be on the same subnet. Pointed DNS address of all servers to DC01.<br/>
<img src="https://github.com/user-attachments/assets/32a44ab5-5728-4f4f-a383-8294ccf2c067" height="80%" width="80%" alt="Launch VMs"/>
<br />
<br />
Installed Active Directory Domain Services on DC01 and server core. Created domain 'corp.local'. Created organizational units and user accounts. Placed user accounts in various OU's.<br/>
<img src="https://github.com/user-attachments/assets/0f1760af-8862-4fb7-b77a-12d908b7ba56" />" height="70%" width="70%" alt="Active Directory Domain"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
