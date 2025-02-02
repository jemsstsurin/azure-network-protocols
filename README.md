<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Observe ICMP traffic
- Configure a Firewall(Network Security Group)
- Observe SSH traffic
- Observe DHCP traffic
- Observe DNS traffic
- Observe RDP traffic

<h2>Actions and Observations</h2>


![image](https://github.com/user-attachments/assets/7af1e6b1-8b0e-4503-a977-ff05bb46ec3b)
![image](https://github.com/user-attachments/assets/b5412408-9729-4f69-8325-e448f80bba9f)



<p>
First you want to install Wireshark on your VM. Then open it and click the Blue Fin at the top left corner to Start Capturing Packets. Within Wireshark filter for ICMP traffic only. Then you retrieve the private IP address of the Ubuntu VM (linux-vm) and attempt to ping it from within the Windows 10 VM. Observe ping requests and replies within WireShark.
</p>
<br />

<img width="1168" alt="Screenshot 2025-02-02 at 5 29 10 PM" src="https://github.com/user-attachments/assets/5fb620b4-c76f-4a23-aa48-98e6eb979db9" />

![image](https://github.com/user-attachments/assets/56285804-a713-48bb-b002-672159ab52a8)



<p>
To configure a Firewall first you want to initiate a perpetual/non-stop ping (by typing "-t" after the private ip address) from your Windows 10 VM to your Ubuntu VM. Next open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic in the setting. In the Action section you're going to click Deny then click Add. To enable ICMP traffic you just delete the rule in the Inbound Security Rule.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
