<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (ICMP, SSH, RDH, DNS, HTTP/S)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 11 (21H2)
- Ubuntu Server 22.04

<h2>High-Level Steps</h2>

- Create a Windows 11 and a Linux (Ubuntu) Virtual Machine in Azure
- Log in to the Windows 11 Virtual Machine and install Wireshark
- Open Wireshark and observe different network traffic
  - Observe IMCP traffic
  - Configure a firewall on the Linux VM and observe SSH traffic
- Step 4

<h2>Actions and Observations</h2>


<p>
Create a Windows and a Linux Virtual Machine in Azure. Make sure they are on the same Virtual Network. 
</p>
<br />


![6-1](https://github.com/user-attachments/assets/ab7271d0-03d6-410a-b69c-5e09f668ca2a)
_______________________________________________________________________________________
![6-1a](https://github.com/user-attachments/assets/d343a29c-c937-46e3-83b5-a7add8ddf430)


<p>
Log in to the Windows 11 Virtual Machine and install Wireshark from www.wireshark.org. Wireshark logs all the packets travelling across the network.
</p>
<br />


![6-2](https://github.com/user-attachments/assets/4f822786-a979-434b-b9f0-47db506257f9)


<p>
Open Wireshark and observe different network traffic. First filter the ICMP traffic in Wireshark then use the private IP address to ping the Linux Virtual Machine in Power Shell.
In the log you can see the four requests from the Windows 11 VM (private IP address 10.0.1.4) and the four replies from the Linux VM (private IP address 10.0.2.4).
</p>
<br />


![6-3](https://github.com/user-attachments/assets/49b5bfe0-5e0d-4779-bd83-67879f66c98d)
_______________________________________________________________________________________
![6-3a](https://github.com/user-attachments/assets/b7787200-1486-4611-aec8-30b5ea6304ca)


<p>
Start a continuous ping in Power Shell. Then go the the Network Security Group in the Network Setting for the Linux VM and add a rule that denies pings in the Inbound Security Rules tab on the left under Settings. Now go back to Power Shell in the VM. Because ping was denied the 
</p>
<br />


![6-4](https://github.com/user-attachments/assets/24901e36-4e57-4a12-b545-752bcbb4e0b4)
_______________________________________________________________________________________
![6-4a](https://github.com/user-attachments/assets/1503c86f-c5be-4475-b22c-d53284b61f8f)
_______________________________________________________________________________________
![6-4b](https://github.com/user-attachments/assets/dcec72f5-3fb0-4b2f-9211-72d9ae28d419)


<p>
Samples line
</p>
<br />


<p>
Samples line
</p>
<br />


<p>
Samples line
</p>
<br />


<p>
Samples line
</p>
<br />


<p>
Samples line
</p>
<br />


<p>
Samples line
</p>
<br />





