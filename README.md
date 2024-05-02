<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, I observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


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

- Create Resource groups in Azure Environments. 
- Develop both Virtual Machines 1 and 2. (Windows And Linux) 
- Remote Desktop Into Virtual Machine 1 and Ping Virtual Machine 2 with Powershell. 
- Use Wireshark to observe, and filter various network traffic. 

<h2>Actions and Observations</h2>

1. (Windows And Linux VM created Provison Of Resources Complete)
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/9c8d62b3-1297-45aa-a25c-2e18ad5a184b)

1. (Cont'd) Windows And Linux VM created Provison Of Resources Complete)
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/5118dc7d-2d82-4ed9-9927-5fbf9ab374a6)

2. (Wired Into VM1 using Public IP Address)
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/6a200ce4-c8b5-40e6-9ee2-b8c0728e4cd8)

3. (Installed WireShark On CM And Now Capturing Live Traffic.)
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/9f5a828b-3e47-44ed-b36a-c7476e3c46d3)

4. (Filtering For ICMP Traffic Without Pinging VM2 yet)
https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/29c19a36-0e4d-4182-8d9c-843b1fc7d48d)

5. Pingged VM2 (Linux Virtual Machine) In powershell using VM'2 Private IP and got a reply.)
https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/0dfc7eb9-1c66-411d-934d-794f3f3b783f)

6. (Went Into VM2 (Linux Virtual Machines) NSG (Network Security Group) Settings and Denied Inbound ICMP taffic and adjusted priority to trigger before SSH Rule.)
https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/aecba45d-1c91-42b8-ab87-315f4bae08ae)

7. (Results of Ping timing out after denying ICMP traffic from VM2 Firewall)
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/cf44a8d4-7514-4cae-a664-e04ae4e14cc1)

8. (Now Filtering Though SSH Via Wireshark to observe additional network)
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/a4e8dea4-1b02-44f5-bfd0-c4ba5dfd281f)

9. Connnected VIA SSH scripted in powershell
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/7031c659-4367-4312-8f88-fbe32d438e77)

10. (Filtering for DHCP Traffic Via Wireshark)
(https://github.com/AndreJohnson2/azure-network-protocols/assets/168602796/8049782e-8232-4d07-9819-c410839ee883)




   




  
<br /># azure-network-protocols
