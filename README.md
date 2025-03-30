## Welcome to Microsoft EntraID Lab
<img src="https://imgur.com/BU8QJcj.png"/>

### Introduction
Today we are going to be setting up multiple indemand technologies.

The lab deploys a Microsoft Sentinel workspace and ingests event logs from the Vitual machine (honeypot) to showcase various types of attacks that are hitting this VM and also to showcase Microsoft Sentinel features. 
You should expect very little or no cost at all due to the size of the data (~10 MB), and the fact that Microsoft Sentinel offers a 30-day free trial on new workspaces.

-->

### Prerequisites
- Microsoft Azure subscription
- Hyper-V
<!-- 
- Network analysis tools (Wireshark, Advanced IP Scanner) for capturing and examining network traffic.
- Network Documentation (Packet Tracer, GitHub)
-->

### Modules
<!--
- <a href="https://github.com/TechGiovanni/Microsoft-Azure-Sentinel-Security-Lab/blob/main/Module%201%20-%20Setting%20up%20the%20environment.md" target=”_blank”>Module 1 - Setting up the environment</a>
- <a href="https://github.com/TechGiovanni/Microsoft-Azure-Sentinel-Security-Lab/blob/main/Module%202%20-%20Configuring%20the%20Virtual%20Machine.md" target=”_blank”>Module 2 - Configuring the Virtual Machine</a>
- <a href="https://github.com/TechGiovanni/Microsoft-Azure-Sentinel-Security-Lab/blob/main/Module%203%20-%20Setup%20Azure%20Monitor%20and%20Log%20Analytics%20custom%20log%20table.md" target=”_blank”>Module 3 - Setup Azure Monitor and Log Analytics custom log table</a>
- <a href="https://github.com/TechGiovanni/Microsoft-Azure-Sentinel-Security-Lab/blob/main/Module%204%20-%20Configure%20Microsoft%20Sentinel%20and%20setup%20the%20Map.md" target=”_blank”>Module 4 - Configure Microsoft Sentinel and setup the Map</a>
-->

# Module 1: Setup Hands the Lab environment

In this section we are goign to setup our Hyper-V, virtual machines, Virtual network adaters, windows server 2022, 


Download the windows Server 2022 ISO from Microsoft and save it to your desktop: 
https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022


Install Hyper-V on windows:
- Go to the search box of your windows machine and type: "Turn Windows features on or off"
- Scroll down and click the check box for Hyper-V
- Click ok

<p align="center">
  <img src="https://imgur.com/KIesN4r.png"/>
</p>


Setting up an external virtual switch in Hyper-V. This allows us to communicate to the internet.
- Click Virtual Switch Manager
- Under Create Virtual Switch, choose External
- Click Create Virtual Switch
- Name it: External_Internet_Switch
- Then click Apply
  

<p align="center">
  <img src="https://imgur.com/gacxDhZ.png"/>
</p>

To avoid ay errors in the future, we will disable 
- Right click the windows icon
- then click device manager

<p align="center">
  <img src="https://imgur.com/GCJqlz8.png"/>
</p>

- Under Network adapters
- Right click "Hyper-V Virtual Ethernet Adapter #2" and then go to "Properties"
- Click the advanced tab
- and then disable "Large Send Offload Version 2 (IPv4)" and "Large Send Offload Version 2 (IPv6)"

<p align="center">
  <img src="https://imgur.com/q0Ctu57.png"/>
</p>


Installing Windows Server 2022



























