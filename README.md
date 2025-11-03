<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (IMCP, SSH, RDH, DNS, HTTP/S)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 11 (21H2)
- Ubuntu Server 22.04

<h2>High-Level Steps</h2>

- Create a Windows 11 and a Linux (Ubintu) Virtual Machine in Azure
- Log in to the Windows 11 Virtual Machine and install Wireshark.
- Open Wireshark and observe different network traffic.
  - IMCP
  - 
- Step 4

<h2>Actions and Observations</h2>


<p>
Create a Windows and a Linux Virtual Machine in Azure. Make sure they are on the same Virtual Network. 
</p>
<br />


![6-1](https://github.com/user-attachments/assets/df1fabd3-2cb4-4e16-9eb2-cc12bcd856f5)
________________________________________________________________________________________
![6-1a](https://github.com/user-attachments/assets/d8e07553-1ea9-43b4-b1d6-7f37f15a6249)


<p>
Log in to the Windows 11 Virtual Machine and install Wireshark from www.wireshark.org. Wireshark logs all the packets travelling across the network.
</p>
<br />


![6-2](https://github.com/user-attachments/assets/4f822786-a979-434b-b9f0-47db506257f9)


<p>
Open Wireshark and observe different network traffic. First filter the ICMB traffic in Wireshark then use the private IP address to ping the Linux Virtual Machine in Power Shell.
In the log you can see the four requests from the Windows 11 VM (private IP address 10.0.1.4) and the four replies from the Linux VM (private IP address 10.0.2.4).
</p>
<br />


![6-3a](https://github.com/user-attachments/assets/de2a8410-b5db-4b0c-a2f7-46bbdf4c761c)


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


<p>
Samples line
</p>
<br />





