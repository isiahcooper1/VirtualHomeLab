<h1>Virtual Home Lab</h1>

<h2>Description</h2>
This project documents the deployment of a virtualized home lab simulating a small enterprise environment.
<br />
The objective was to design and configure core infrastructure including a Domain Controller, domain-joined client machine, DNS, and internal networking using a hypervisor.
<br />
This lab demonstrates foundational system administration skills including server deployment, IP configuration, domain setup, and client authentication. <br>
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
1. Launched 3 VMs in Hyper-V - One UI-based domain controller, one server core domain controller, and one file server. <br />
2. Installed Windows Server 2022 on all 3 servers. <br />
3. Created an external virtual switch and configured all 3 VMs to use the same switch. <br />
<img src="https://github.com/user-attachments/assets/32a44ab5-5728-4f4f-a383-8294ccf2c067" height="80%" width="80%" alt="Launch VMs"/>
<br />
<br />
1. Configured all 3 servers to be on the same subnet. <br />
2. Pointed DNS address of all servers to DC01. <br />
<img src="https://github.com/user-attachments/assets/4af0147a-6579-4aae-8361-41b00be8e099" height="80%" width="80%" alt="Server Network"/>
<br />
<br />
Installed Active Directory Domain Services on DC01 and server core. Created domain 'corp.local'. Created organizational units and user accounts. Placed user accounts in various OU's.<br/>
<img src="https://github.com/user-attachments/assets/0f1760af-8862-4fb7-b77a-12d908b7ba56" height="80%" width="80%" alt="Active Directory Domain"/>
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
