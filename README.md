<h1>Virtual Home Lab</h1>

<h2>Description</h2>
This project documents the deployment of a virtualized home lab simulating a small enterprise environment. 
<br>
<br>
The objective was to design and configure core infrastructure including a Domain Controller, domain-joined client machine, DNS, and internal networking using a hypervisor.
<br>
<br>
This lab demonstrates foundational system administration skills including server deployment, IP configuration, domain setup, and client authentication.
<br>
<br>


<h2>Utilities Used</h2>

- <b>Hyper-V</b> 
- <b>Active Directory Domain Services (AD DS)</b>
- <b>DNS Server</b>
- <b>DHCP Server</b>
- <b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows Server 2022</b>
- <b>Windows 11</b> (21H2)
- <b>External Virtual Network</b>
- <b>Static IP configuration for server infrastructure</b>

<h2>Walk-through:</h2>
<br>
<p align="center">
1. Launched 2 VMs in Hyper-V - One server (DC01) and one client. <br />
 <br>
2. Installed Windows Server 2022 on server and Windows 11 on client. <br />
 <br>
<img src="https://github.com/user-attachments/assets/32a44ab5-5728-4f4f-a383-8294ccf2c067" height="80%" width="80%" alt="Launch VMs"/>
<br />
<br />
3. Created an external virtual switch and configured both the server and the client to use the same switch. <br />
 <br>
4. Configured server (DC01) and client to be on the same subnet. <br />
 <br>
5. Pointed DNS address of client to server. <br />
 <br>
<img src="https://github.com/user-attachments/assets/4af0147a-6579-4aae-8361-41b00be8e099" height="80%" width="80%" alt="Server Network"/>
<br />
<br />
6. Installed Active Directory Domain Services and DNS roles on server (DC01). 
 <br>
7. Created domain 'corp.local'.
 <br>
8. Promoted DC01 to domain controller.
 <br>
<img src="https://github.com/user-attachments/assets/11ee8e29-8147-4756-a59f-0c93214158ef" width="80%" alt="Active Directory"/>
<br />
<br />
9. Joined WIndows 11 client to the domain.<br/>
 <br>
<img src="https://github.com/user-attachments/assets/0f1760af-8862-4fb7-b77a-12d908b7ba56" height="80%" width="80%" alt="Active Directory Domain"/>
<br />
<br />
10. Configured Active Directory-integrated Forward and Reverse Lookup Zones to provide authoritative internal DNS resolution for the domain.  <br/>
 <br>
<img src="https://github.com/user-attachments/assets/9c2c1acf-352d-4513-8b5f-b728289683d3"  height="80%" width="80%" alt="DNS Forward Lookup"/>
 <br>
<img src="https://github.com/user-attachments/assets/938185e3-7ced-4391-8919-b51d22e797ba" height="80%" width="80%" alt="DNS reverse Lookup"/>
<br />
<br />
11. Implemented static IP configuration (192.168.1.250) for the DNS server and configured domain-joined clients to use the internal DNS server for proper authentication and Group Policy processing. <br/>
  <br>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
