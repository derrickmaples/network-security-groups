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
  - Observe IMCP traffic then configure a firewall on the Linux VM
  - Observe SSH traffic
  - Observe RDH traffic
  - Observe DNS traffic
  - Observe HTTP/S traffic
  

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
Observe SSH traffic from the Linux VM. This filter records traffic from a specific machine using port 22. Log in to the Linux VM in Power Shell. In Wireshark you will see every key stroke you make is recorded. 
</p>
<br />


![6-5](https://github.com/user-attachments/assets/46d8cd02-63ce-42e5-b966-7946d8983e20)
_______________________________________________________________________________________
![6-5b](https://github.com/user-attachments/assets/c2863d21-08a3-4b76-8949-b4a27594be18)


<p>
Observe RDH traffic of the Windows 11 VM. Enter "tcp.port == 3389" into the filter. You see Windows is constantly stream information unlike SSH, which only sends info when an action is done.
</p>
<br />


![6-7](https://github.com/user-attachments/assets/3bb82507-9d59-42d8-a48c-6db3372a8c1e)


<p>
Enter nslookup followed by a website (google.com for the purposes of this project) in Power Shell to observe DNS traffic. You will be able to see the IP address or addresses for the website. 
</p>
<br />


![6-6](https://github.com/user-attachments/assets/9a596fa9-9672-47c7-9cea-70762d25ed97)


<p>
Observe HTTP/HTTPS traffic. This records all web traffic in the VM. HTTPS encryps the HTTP data. To filter HTTPS specifically enter "tcp.port == 443".
</p>
<br />


![6-8](https://github.com/user-attachments/assets/30f3afc1-b9ce-4e91-ba53-e9a5542ea627)
_______________________________________________________________________________________
![6-8a](https://github.com/user-attachments/assets/59162664-9b31-4175-8587-b006d587c9ab)


<h2>Success!</h2>
