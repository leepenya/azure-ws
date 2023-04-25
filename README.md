<p align="center">
<img src="https://imgur.com/38XGamW.png" height="60%" width="40%" alt="Wireshark Logo"/>
</p>

<h1>Inspecting Network Protocols with Wireshark</h1>
Summary: In this project, I inspected several network protocols (ICMP, SSH, DHCP, DNS and RDP) using the protocol analyzer Wireshark.<br />

<h2>Requirements</h2>

- Computer with internet connection
- Microsoft Azure account
  - Credit card to set up the account
  
 <h2>Environments & Technologies Used</h2>
 
 - Microsoft Azure (Virtual Machines/Network Security Groups)
 - Remote Desktop
 - Wireshark
 - Windows command line & PowerShell
  
 <h2>Operating Systems Used</h2>
 - Windows 10 (VM1)
</br>
 - Ubuntu Server 20.04 (VM2)
 
  <h2>High-level Steps</h2>
  
1. Set up a network with two virtual machines (VMs) in Microsoft Azure.
2. Install Wireshark on one virtual machine (VM1).
3. Use Wireshark to inspect ICMP, SSH, DHCP, DNS and RDP traffic.

<h2>Specific Steps</h2>
<p>
<img src= "https://imgur.com/7qbWlgX.png" height="80%" width="80%" alt="Azure Network"/>
</p>
<p>
1. First, I set up a network with two VMs (one running Windows 10 and the other Ubuntu Server 20.04) in Microsoft Azure and viewed the network topology generated (see above).
</p>
</br>

<p>
<img src= "https://imgur.com/J4yPUGD.png" height="80%" width="80%" alt="Wireshark-ICMP-1"/>
</p>
<p>
2. I then installed Wireshark on the Windows VM (VM1) and used Remote Desktop to connect my host machine to VM1. Once inside Wireshark, I filtered for ICMP traffic, pinged from VM1 (IP address 10.0.0.4) to VM2 (IP address 10.0.0.5), and observed the resulting traffic in Wireshark.
</p>
<br/>

<p>
<img src= "https://imgur.com/lyRiw89.png" height="80%" width="80%" alt="Wireshark-ICMP-2"/>
</p>
<p>
3. Next, I pinged the University of Texas from VM1 and observed the ICMP traffic generated.
</p>
</br>

<p>
<img src= "https://imgur.com/qZeSs1Z.png" height="80%" width="80%" alt="Deny-Inbound-ICMP"/>
</p>
<p>
4. I then created an inbound security rule in VM2 blocking ICMP traffic from VM1.
</p>
</br>

<p>
<img src= "https://imgur.com/PIaeFOy.png" height="80%" width="80%" alt="Deny-Inbound-ICMP"/>
</p>
<p>
5. In this step, I observed the effect of the security rule on ICMP traffic.
</p>
</br>

<p>
<img src= "https://imgur.com/lLS6nu5.png" height="80%" width="80%" alt="SSH-traffic"/>
</p>
<p>
6.  Next, I filtered for SSH traffic, connected VM1 to VM2 using SSH, and executed a few commands to see their effect on the network traffic in Wireshark.
</p>
</br>

<p>
<img src= "https://imgur.com/lwGBjrX.png" height="80%" width="80%" alt="DHCP-traffic"/>
</p>
<p>
7.  I then filtered for DHCP traffic in Wireshark, requested a new IP address from VM1's command line, and observed the resulting network traffic in Wireshark.
</p>
</br>

<p>
<img src= "https://imgur.com/T1fzZlB.png" height="80%" width="80%" alt="DHCP-traffic"/>
</p>
<p>
8.  Here, I filtered for DNS traffic in Wireshark, generated DNS traffic by checking Google and Yahoo's IP addresses, and then observed the ensuing DNS traffic.
</p>
</br>

 <p>
<img src= "https://imgur.com/0G7r7vy.png" height="80%" width="80%" alt="RDP-traffic"/>
</p>
<p>
9.  Finally, I filtered for RDP traffic in Wireshark and noted that the traffic was continuous because of the live stream between my host computer and VM1.
<p>Thanks for checking out my first Wireshark lab!
</p>
