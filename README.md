<h1>HoneyPot_SIEM_Monitoring_</h1>

<h2>Description</h2>
In this Home Lab, I set up a basic home SOC in Azure from scratch. Using a free Azure subscription, I create a virtual machine (VM), opening it to the internet as a honeypot, and forwarding logs to a central repository. I then integrate Microsoft Sentinel to analyze real-world attack data and then go ahead to create an automation rule for Security Incidents.
<br />
<br />

<b>Evidence Collected</b>
  
- <b>Security event logs (Event ID 4625)</b>
- <b>Source IP addresses</b>
- <b>Geographical location data</b>
- <b>Timestamps of malicious activity</b>

<b>Lessons Learned</b>

- <b>Importance of proper log collection and centralization</b>
- <b>Effectiveness of visualization for security monitoring</b>
- <b>Need for automated alerting on suspicious activity</b>

<b>Next Steps</b>

- <b>Continue monitoring for additional unauthorized access attempts</b>
- <b>Expand logging to include other security events</b>
- <b>Create automated Sentinel playbooks for similar incidents</b>

<b>Closure</b>
- This incident is considered resolved as the unauthorized access attempts were expected behavior in the honeypot environment. No production systems were impacted. The lab successfully demonstrated Azure Sentinel's capabilities for detecting and investigating security incidents.
  
<br />

<h2>Environment</h2>

- <b>Azure</b>

- <b>Microsoft Sentinel</b>

- <b>Remote Desktop</b>
  
<h2>Languages Used</h2>

- <b>Kusto Query Language(KQL)</b>
  
<h2>Program walk-through:</h2>

<p align="center">
Resource Group created in Azure: <br/>
<img src= "https://imgur.com/BJFaXXi.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
Virtual Network created in Azure  <br/>
<img src= "https://imgur.com/sZul9rl.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
Remote Desktop-Azure Virtual Machine <br/>
<img src= "https://imgur.com/8Ky94Ye.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
Windows firewall turned off to allow for unfiltered inbound traffic  <br/>
<img src= "https://imgur.com/73VRka8.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
Screenshot showing failed attempts from different users globally  <br/>
<img src= "https://imgur.com/TARw049.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
Filtered Security Events based on IPaddresses from different Geolocations  <br/>
<img src= "https://imgur.com/WxGd4fW.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
Attack Map creation with Json script  <br/>
<img src= "https://imgur.com/NGvyy6N.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />  
VM Attack Map at the time of creation <br/>
<img src= "https://imgur.com/ILEhTSf.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br /> 
VM Attack about 18 hours later  <br/>
<img src= "https://imgur.com/aeLwPYJ.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br /> 
VM Attack Map about 30 hours later <br/>
<img src= "https://imgur.com/jIoDLjB.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br /> 
Incidents report from the attacks <br/>
<img src= "https://imgur.com/sPhsXrh.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
Automation to Change status and Assign once incident is detected <br/>
<img src= "https://imgur.com/ove7THC.png" height="80%" width="80%" alt="HoneyPot"/>
<br />
<br />
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

