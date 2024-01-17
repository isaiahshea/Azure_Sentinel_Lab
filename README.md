<h1>Geolocation SIEM Monitoring Failed RDM with Azure Sentinel</h1>


<h2>Description</h2>
<b>In this Microsoft Azure project, I established a virtual machine as a honeypot, strategically configuring its firewall to attract and capture RDP and brute force attacks. Leveraging Windows Event Viewer and Microsoft Sentinel, I seamlessly aggregated and normalized the attack data. Through a custom PowerShell script and external API, I pinpointed the exact geographical locations of malicious actors, enriching the security analysis. The SIEM system was then fine-tuned to upload these log insights onto a map, offering a visual and dynamic representation of global cyber threats.
</b>
<br />
<br />
The PowerShell script in this repository is designed to extract details from Windows Event Logs regarding unsuccessful RDP attacks. It then utilizes a third-party API to gather geographic information about the location of the attackers.
<br />
<br />

<p align="center">
<img src="https://imgur.com/1co4vFs.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<h2>Platforms and Tools Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer
- <b>Microsoft Azure:</b> Hosted a honeypot virtual machine and configured firewall settings for RDP and brute force attacks.
- <b>Microsoft Sentinel:</b> Implemented as a SIEM solution, integrated with Windows Event Viewer for real-time threat detection and analysis.
- <b>Microsoft Log Analytics:</b> Utilized for aggregating and normalizing event data, enhancing security insights through centralized log analysis.
<p align="center">
<img src="https://imgur.com/rQCpOFv.png" height="85%" width="85%" alt="Log Analytics Workspace"/>
</p>
<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<p align="center">
<img src="https://imgur.com/fFALpcr.png" height="85%" width="85%" alt="ipgeolocation.io"/>
</p>

<h2>Honeypot Firewall Configuration</h2>

<p align="center">
<img src="https://imgur.com/VRc1SOC.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>RDP attacks incoming; Custom logs being output with geodata in VM</h2>

<p align="center">
<img src="https://imgur.com/yqnqChV.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>Monitor Brute Force Entries in MS Sentinel; SIEM Tuning: Log Aggregation Actions </h2>

<p align="center">
<img src="https://imgur.com/yiGjfws.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://imgur.com/a1t8r7L.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
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
