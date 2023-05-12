<p align="center">
<img src="https://imgur.com/4Cm6yiK.png alt="Traffic Examination"/>  
</p>

<h1>Azure Virtual Machines Traffic Inspection</h1>
Hello! In this tutorial I observe and explore several network traffic protocols between two Azure Virtual Machines with Wireshark. This excercise helps those who want to learn about network protocols and how to observe network traffic such as: </p>                                                               

- DNS
- SSH
- DHCP
- ICMP
- RDP
<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines) abbreviated VM. VMs are used to install the software that is used to analyze the traffic being sent.

- Remote Desktop Protocol (RDP) is used to connect to the virtual machines and it is one type of traffic observed in wireshark. 

- Various Command-Line Tools are used such as Command Prompt for ping commands and Powershell to ssh into the second virtual machine.

- Network Protocols (SSH, RDH, DNS, ICMP, DHCP) are observed in wireshark as both VMs communicate with each other under various commands.

- Wireshark is the network traffic analyzer used to observe the different types of traffic being sent between both VMs.

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Pre-Requisites</h2>
<h2>Creating the virtual machines<h2/>                                                             



Log into

<p>
<img src="https://imgur.com/pzsx4Xn.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/Hz2NxI2.png alt"Rescource Group"/?
</p>
<br />

Step 4 - After logging in to the VM, navigate to Microsoft Edge and install Wireshark 

<p>
<img src="https://imgur.com/clrmTgG.png alt"Rescource Group"/?
</p>

<p>
<img src="https://imgur.com/plnj4UI.png alt"Rescource Group"/?
</p>
<br />
<br />
Now that you have logged in you can continue on to the traffic observation steps detailed below. 


<h2>Actions and Observations</h2>
These observations are made by inputting commands that corresond to the type of traffic one wishes to observe and then filtering Wireshark by the corresponding traffic type.
<br />
<br />

Below is RDP (Remote Desktop Protocol) traffic observation after filtering for RDP traffic in Wireshark 

<p>
<img src="https://imgur.com/CHAA6zi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below is DHCP (Dynamic Host Control Protocol) traffic observation using Wireshark

<p>
<img src="https://imgur.com/Gi74JxZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below is DNS (Domain Name System) traffic observation using Wireshark

<p>
<img src="https://imgur.com/NQQTI7C.png " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below is SSH (Secure Shell) traffic observation using Wireshark

<p>
<img src="https://imgur.com/2lxIu4v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Below are the steps for ICMP (nternet Control Message Protocol) traffic observation from a perpetual ping and ICMP traffic stop after the inbound firewall rule is set 
<br />
1. Set the perpetual ping comand to ping VM2 and observe the ICMP traffic
<p>
<img src="https://imgur.com/cgRnPPG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />

2. Change the Inbound firewall rule to deny ICMP traffic

<p>
<img src="https://imgur.com/gKmvkuS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />


3. Observe the ping request times out after the firewall rule was put in place
(*note - The ping request timed out due to the ICMP traffic being denied as the firewall rule blocked the traffic)
<p>
<img src="https://imgur.com/dMWGgWi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
