# Date :28.10.2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
<img width="837" height="462" alt="Screenshot 2026-10-28 112818" src="https://github.com/user-attachments/assets/f8a28d99-f290-40c1-a130-24bd18bfce71" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>

## configuration:
## LAN 1
<img width="818" height="462" alt="Screenshot 2026-10-28 112848" src="https://github.com/user-attachments/assets/1f33bc20-2c99-41f0-a1ca-8b605cb48bfa" />
<img width="822" height="465" alt="Screenshot 2026-10-28 112906" src="https://github.com/user-attachments/assets/6f86b380-08ea-429b-8718-79589fe29ce7" />
<img width="818" height="463" alt="Screenshot 2026-10-28 112933" src="https://github.com/user-attachments/assets/f523fd2f-e4c4-4662-83ea-e5c3fa5722c6" />

## LAN 2
<img width="826" height="471" alt="Screenshot 2026-10-28 113000" src="https://github.com/user-attachments/assets/a0c9df08-4b08-44c7-a8ac-28e3e75ad1e3" />
<img width="817" height="488" alt="Screenshot 2026-10-28 113017" src="https://github.com/user-attachments/assets/50b12d45-61b7-44e5-8b33-fd28f285fb4c" />
<img width="827" height="467" alt="Screenshot 2026-10-28 113039" src="https://github.com/user-attachments/assets/d139573d-2d07-4513-97ee-dd5b75f7affe" />

## SWITCH 
<img width="815" height="456" alt="Screenshot 2026-10-28 113136" src="https://github.com/user-attachments/assets/3de1151e-99f9-4391-b63d-547159834bd0" />
<img width="822" height="465" alt="Screenshot 2026-10-28 113216" src="https://github.com/user-attachments/assets/1ea40a35-6dbd-4ece-a6ad-7467396d0ad6" />

## ROUTER
<img width="817" height="456" alt="Screenshot 2026-10-28 113236" src="https://github.com/user-attachments/assets/456bcab3-7e9d-4f13-b755-0bea9864fcc5" />

## PING:
# LAN 1
<img width="822" height="466" alt="Screenshot 2026-10-28 113258" src="https://github.com/user-attachments/assets/985a12cd-f506-4373-9370-a1a76254a8d9" />
<img width="822" height="517" alt="Screenshot 2026-10-28 113316" src="https://github.com/user-attachments/assets/178a3d6f-0454-4c45-b8fc-90698182b275" />
<img width="798" height="461" alt="Screenshot 2026-10-28 113331" src="https://github.com/user-attachments/assets/8505dd5e-9860-44e2-b03e-9cc405e08cf5" />

## LAN 2
<img width="816" height="466" alt="Screenshot 2026-10-28 113349" src="https://github.com/user-attachments/assets/b6370934-61dd-4537-8da3-5866fab930fd" />
<img width="820" height="456" alt="Screenshot 2026-10-28 113410" src="https://github.com/user-attachments/assets/67459217-9d9f-4424-aada-82ce4ff7abfb" />
<img width="816" height="455" alt="Screenshot 2026-10-28 113426" src="https://github.com/user-attachments/assets/f9c393ab-1487-4347-8ef7-bc265da7a8ab" />

## BOTH LAN:
<img width="816" height="472" alt="Screenshot 2026-10-28 113445" src="https://github.com/user-attachments/assets/bd6deb39-ceb2-4f3b-8203-de58151681fa" />
<img width="821" height="465" alt="Screenshot 2026-10-28 113501" src="https://github.com/user-attachments/assets/c9c61a3d-67de-4b2c-808c-24b4b6e90ab3" />

## SWITCH 0
<img width="818" height="460" alt="Screenshot 2026-10-28 113516" src="https://github.com/user-attachments/assets/38253c5c-8856-42a7-9578-77385bae024e" />

## SWITCH 1
<img width="820" height="152" alt="Screenshot 2026-10-28 113528" src="https://github.com/user-attachments/assets/84b6b0f6-f128-4276-8779-22b20c078037" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

