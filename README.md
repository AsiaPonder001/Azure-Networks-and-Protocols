<p align="center">
<img src="https://i.imgur.com/wJ6cg4s.png">
</p>

<h1>Azure Virtual Machines Traffic Inspection</h1>
Hello! In this tutorial I observe and explore several network traffic protocols between two Azure Virtual Machines with Wireshark. This excercise helps those who want to learn how to observe network traffic and use protocols such as: </p>                                                               

- DNS (Domain Name System; Port 53)
- SSH (secure shell ; Port 22)
- DHCP (Dynamic Host Configuration Protocol; Port 67 & 68)
- ICMP (Internet Control Messaage Protocol; No Port #)
- RDP (Remote Desktop Protocol; Port 3389)
<br />

<b> You will need a VM with Windows and another VM with Ubuntu. This tutorial assumes you have already created those two virtual machines. Need to create Virtual Machines?
                                                                 
<a href="https://github.com/AsiaPonder001/Resource-Groups-and-V-Ms">CLICK HERE</a>

<img src="https://i.imgur.com/xocmOjp.png">
</p>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure Virtual Machines

- Remote Desktop Protocol

- Network Protocols (SSH, RDH, DNS, ICMP, DHCP)

- Wireshark is the network traffic analyzer used to observe the different types of traffic being sent between both VMs.

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Linux/Ubuntu Server 20.04 


<h2> Sign into the Windows VM </h2>

<b> Copy Public ip address and paste it into the RDP connection </b>

<img src="https://i.imgur.com/K79BJvW.png">

<b>After logging in to the VM, navigate to Microsoft Edge and install Wireshark </b>

<img src="https://i.imgur.com/It0Ez7A.png">
<p>
<img src="i.https://imgur.com/IBt3KUh.png">
<img src="https://i.imgur.com/7PlTD8N.png">
</p>
<br /> 


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
