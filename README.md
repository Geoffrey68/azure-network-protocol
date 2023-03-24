# azure-network-protocol
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

- Step 1 Observe network traffic with Wireshark
<p>
Connect to Virtual Machine 1 (VM1) with remote desktop
<p>
Download Wireshark and observe all traffic
<p>
<img src="https://i.imgur.com/yLBRiHL.png"/>
<p>
  </p>
  
From VM-1 using Powershell, ping VM-2's private IP address and observe ICMP traffic in Wireshark
<p>
<img src="https://i.imgur.com/ZZU8Zqc.png"/>
<p>
  
Initiate a perpetual/non-stop ping from your Windows 10 VM-1 to your Ubuntu VM-2
<p>
<img src="https://i.imgur.com/kSfZBz8.png"/>
<p>
Open the Network Security Group your Ubuntu VM-2 is using and disable incoming (inbound) ICMP traffic
<p>
<img src="https://i.imgur.com/SiChTTw.png"/>
<p>
Back in the Windows 10 VM-1, observe the ICMP traffic in WireShark and the command line Ping activity
<p>
  
  <img src="https://i.imgur.com/nWveNMw.png"/>
<p>
  
Re-enable ICMP traffic for the Network Security Group your Ubuntu VM-2 is using
<p>
<img src="https://i.imgur.com/xG6xuWk.png"/>
<p>
Back in the Windows 10 VM-1, observe the ICMP traffic in WireShark
<p>
<img src="https://i.imgur.com/p0tpFCS.png"/>
<p>
  Back in Wireshark, filter for SSH traffic only
  <p>
    
From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address)
    <p>
      
      <img src="https://i.imgur.com/txU8PbF.png"/>
      <p>
        
      
Type commands into the linux SSH connection and observe SSH traffic spam in WireShark
<p>
  <img src="https://i.imgur.com/YxsroUL.png"/>
  <p>
    
  
  
- Back in Wireshark, filter for DHCP traffic only
  <p>
From your Windows 10 VM, attempt to issue your VM a new IP address from the command line (ipconfig /renew)
    <p>
Observe the DHCP traffic appearing in WireShark
      <p>

- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
