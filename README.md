<h1>Security Incident Event Management Lab in Azure</h1>

<br />

<h2> Content for SIEM home lab </h2>

- <b>Project Description</b> 
- <b>Languages and Utilities used</b>
- <b>Programe walk through</b>
- <b>Conclusion</b>


<h2>Project Description</h2>
In this project, I set up a microsoft Azure Sentinel a SIEM tool to recieve logs from a cloud based Virtual Machine with its firewall purposely turned off making it vulnerable to attacks. 
We monitor failed login attempts to the server by collecting different IP addresses accross the globe. The extracted Ip addresses is then mapped to visualise all incoming attacks.


<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Azure Portal</b>
- <b>Azure Sentinel</b>
- <b>Kusto Query Language</b>
- <b>Network Security groups</b>

  
<h2>Program walk-through:</h2>

<p align="left">
1. Create an Azure account and set up your virtual machine: <br/>
<img src="https://i.imgur.com/i7EUH6I.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Setup an Azure resource group and label it (in this case Honeypot labe) - to hold resources related to our task for easier management, organisation, and access cpntrol:  <br/>
<img src="https://i.imgur.com/MpRr1M5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. Configure the Network security group settings and set it to allow unrestricted access from the public internet: <br/>
<img src="https://i.imgur.com/IlxNZF2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. We setup a Log Analytics Workspace - to collect, analyse and query log and performance data from the resource group we created:  <br/>
<img src="https://i.imgur.com/MoAP1oW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. Setup and configure Microsoft Defender For Cloud (enabling log collection for All Events) to capture security Logs from the created virtual machine, for Sentinel to analyse:  <br/>
<img src="https://i.imgur.com/C33lzQZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wstmDgH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
6. Setup Azure Microsoft Sentinel - the siem tool used to analyze and visualise the attack data:  <br/>
<img src="https://i.imgur.com/qEMeCFh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/02Z6CXy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7. Log into the virtual machine and analyse event viewer:  <br/>
<img src="https://i.imgur.com/m4XGEjR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
8. Disable the firewall of the virtual machine - reducing its security making it vulnerable to attacks.  <br/>
<img src="https://i.imgur.com/98N79o8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
9. We run a powershell script that collects key artifact (IP addresses) from failed log in attempts. <br/>
The Ip addresses are exported to a third party client that returns the locational data (longitude, latitude).
<img src="https://i.imgur.com/Qj4MwcW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Npdzlqh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
10. We create a custom log based on the failed log in attempts to train Log Analytics on the structure and format of all the data it would recieve.  <br/>
We can then visualise all incoming events from the event viewer through Log Analytics Workspace. (Kusto Query Language)
<img src="https://i.imgur.com/HEvKcT9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/BGkEeac.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
11. We create a new workbook in Microsoft Sentinel to retrive the injested failed login attempts log to be plotted on the map.  <br/>
Once this is done, we can visualize any current attacks to the Virtual Machine.
<img src="https://i.imgur.com/R1DH5sg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/bPb20Pt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
12. I allowed time to passed and left the virtual macjine running for a day to get more data for my research. <br/>
This is a timeline of the attacks
<img src="https://i.imgur.com/UeehxBU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/sWMFv8V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dp8VuPL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2> Conclusion </h2>
To conclude, through the setup of the virtual machine in Azure portal and leveraging  Azure Sentinel for log analysis,
I was succesffuly able to track and visualise attempted attacks on the system. By exporting the data into Sentinel, I identified key 
attack vectors and pinpointed the geographic locations from where the attack originated. Utilizing Azure Mitre Framework, I mapped these 
to specific tactics and techniques revealing that the system is vulnerable to techniques T1110 (BRUTE FORCE) and T1531 (Account Access Removal)
<img src="https://i.imgur.com/BCQdhRz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/iTbrvXm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
This analysis highlights the importance of proactive monitoring and vulnerability management in cloud environments, 
and the need for robust defense strategies to mitigate such attacks. Further work could focus on implementing recommended 
security measures to address these vulnerabilities and strengthen the overall security posture of the system.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
