<h1>Azure Sentinel SIEM Honeypot Lab</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

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

<h2>Program walk-through:</h2>

<p align="center">
Created Resouce Group in Azure: <br/>
<img src="https://i.imgur.com/yrwFL7g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

You may be asking why should I create a resource group first and why not the virtual machine right away.
This is because in Azure we will be creating a lot of resources and from my experience it is easier to setup a new resource group as this will make it a lot easier later in this lab.

To create a new resource group, click on the resource groups button

<br />

<p align="center">
<img src="https://i.imgur.com/hFqBqXC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Click on the resource group button to create your resource group

By default, there will be no resource groups and we will have to create one for this lab.

<br />

Click on the create resource group button and you will be presented with the project details and resource details field that need to be filled in.
NOTE: the default subscription will always be Azure subscription 1 with the free Azure sign up

<p align="center">
<img src="https://i.imgur.com/X6ThREN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br /> 

As I will be using my virtual machine for a honeypot scenario, I have called mine Honeypot-Lab, but you can name your resource group to any name as you wish. anything of your choice.

<p align="center">
<img src="https://i.imgur.com/ebTE1a1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br /> 

NOTE: in the region settings, by default it will be set to (US) EAST US, this is the region where we want to deploy our resource group to a region where the data centre is situated. I set mine to (Europe) UK South as this was the recommended option for myself for the region, I am in.
Then click the review + create button and your new resource group should be created:

<p align="center">
<img src="https://i.imgur.com/lv1mAgM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

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
