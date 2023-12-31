<h1>Azure Sentinel SIEM Honeypot Lab</h1>


<h2>Description</h2>
The purpose of this project is to create a honey pot virtual machine with an open port connection, to allow threat actors to try and RDP connect to the machine, whilst being able to capture sign in logs using a custom created powershell script. And to plot the geogrphical data onto a world map.
<br />

<h2>Objectives</h2>

I used a customer powershell script to extract metadata from windows event viewer, which was forwarded to a third party API in order to derive geolocation data

I configured Log analytics workspace in Azure to ingest custom logs containing geographic information (latitude, longitude, state/province and country)

I configured a workspace with the intent of mapping geo data in Azure Sentinel

I configured azure Sentinel (Microsoft’s SIEM) workbook to display global attack data (RDP brute force) on world map according to physical location and magnitude of attacks.

<br /> 

 <p align="center">
  Mind map of honet pot lab: <br/>
 <img src="https://i.imgur.com/qeH47gn.png" height="80%" width="80%" al="honey pot lab"/>
 <br /> 
 <br /> 

<h2>Software tools used</h2>

- <b>Azure Free Subscription</b>
- <b>Microsfot Defender</b>
- <b>Azure Sentinel (SIEM)</b>
- <b>Windows 10 virtual machine</b>
- <b>Remote Desktop Connection</b>
- <b>Powershell</b>
- <b>IP Geolocation API</b>
- <b>Azure Log Analytics Workspace</b>
- <b>Windows event viewer</b>
- <b>Command Prompt</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<br />

This project will be broken down into sections for setting up each part of the SIEM Honeypot lab and the steps that were taken to acheiving the goal for this lab

<br /> 

1. [Creating a resource group in Azure](https://github.com/Zeeshan-Fraz/Create-a-resource-group-in-azure)
2. [Creating a virtual machine (windows 10)](https://github.com/Zeeshan-Fraz/Creating-a-virtual-machine-windows-10-) 
3. [Creating a log analytics workspace](https://github.com/Zeeshan-Fraz/Creating-a-log-analytics-workspace)
4. [Setting up Microsoft Defender for cloud](https://github.com/Zeeshan-Fraz/Setting-up-Microsoft-Defender-for-cloud-)
 
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
