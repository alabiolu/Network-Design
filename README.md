# SOHO Network Design

## Objective
Design a network for a company to operate separately from the HQ's network with the following requirements:

- One router
- 3 departments
- Each department is required to have different VLANs
- Have a wireless network for the users.
- host devices in the network are required to obtain IPv4 addresses automatically.
- Devices in all departments are required to communicate with each other.

### Skills Learned

- Network design and architecture.
- Subnetting and subnet calculation.
- Development of critical thinking and problem-solving skills in Network design.

### Tools Used

- Packet Tracer.

## Steps
Desing the network by draging and dropping creating the 3 departments needed and connecting them via a cable

![Screenshot 2024-08-03 173833](https://github.com/user-attachments/assets/1ae31f6a-d631-44d1-b971-5aadd11a5747)

*Ref 1: Network Diagram*

Worked out the subnet mask calculation using 2^n having the base network 192.168.1.0 the baseline submask should be 255.255.255.0, this converted to binary equals 11111111.11111111.11111111.00000000
getting the subnet for 3 different department by borrowing 2 bits i have 11111111.11111111.11111111.11000000 when calculated it is translated into decimal i have new subnet mask 255.255.255.192.
to get ip range for the 3 department we use a block size of 64.

## 1st Department
Network ID:192.168.1.0

Broadcast ID:192.168.1.63

Host Range:192.168.1.1 - 192.168.1.62

## 2nd Department
Network ID:192.168.1.64

Broadcast ID:192.168.1.127

Host Range:192.168.1.65 - 192.168.1.126

## 3rd Department
Network ID:192.168.1.128

Broadcast ID:192.168.1.191

Host Range:192.168.1.129 - 192.168.1.190

## Configure Switch
Configure switch to connect all device from all 3 department to it below are the command run on the switch CLI and to create VLAN


![Screenshot 2024-08-03 224028](https://github.com/user-attachments/assets/993aabec-32e2-4d96-80c0-2961d54b5d1b)

*Ref 2: Network Diagram*
