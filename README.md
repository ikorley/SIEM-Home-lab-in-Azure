<h1>Security Incident Event Management Lab in Azure</h1>

<h2>Project Description</h2>
In this project, I set up a microsoft Azure Sentinel a SIEM tool to recieve logs from a cloud based Virtual Machine with its firewall purposely turned off making it vulnerable to attacks. We monitor failed login attempts to the server by collecting different IP addresses accross the globe. The extracted Ip addresses is then mapped to visualise all incoming attacks.


<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Azure Portal</b>
- <b>Azure Sentinel</b>
- <b>Kusto Query Language</b>
- <b>Network Security groups</b>

  
<h2>Program walk-through:</h2>

<p align="center">
Set Up windows 2019 client: <br/>
<img src="https://i.imgur.com/cZXTmBj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Logging in:  <br/>
<img src="https://i.imgur.com/M7n7xW8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Assigning IP for internal address: <br/>
<img src="https://i.imgur.com/ZTYbVGS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup Active Directory (Will take some time):  <br/>
<img src="https://i.imgur.com/MoAP1oW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add a new admin user:  <br/>
<img src="https://i.imgur.com/jGNNbcH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup a remote access server:  <br/>
<img src="https://i.imgur.com/NXqjBwO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup a new DHCP server:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup user accounts using Powershell:  <br/>
<img src="https://i.imgur.com/cMeXEUu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set up client:  <br/>
<img src="https://i.imgur.com/8ybTFFk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Assign client to domain:  <br/>
<img src="https://i.imgur.com/F8xoBPe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
Connecting to domain client:  <br/>
<img src="https://i.imgur.com/SwJj0uP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
