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
Design the network by dragging and dropping creating the 3 departments needed and connecting them via a cable

![Screenshot 2024-08-03 173833](https://github.com/user-attachments/assets/1ae31f6a-d631-44d1-b971-5aadd11a5747)

*Ref 1: Network Diagram*

Worked out the subnet mask calculation using 2^n having the base network 192.168.1.0 the baseline submask should be 255.255.255.0, this converted to binary equals 11111111.11111111.11111111.00000000
getting the subnet for 3 different departments by borrowing 2 bits I have 11111111.11111111.11111111.11000000 when calculated it is translated into decimal i have a new subnet mask 255.255.255.192.
to get IP range for the 3 departments we use a block size of 64.

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
Configure the switch to connect all devices from all 3 departments to it below are the commands run on the switch CLI to configure VLAN


![Screenshot 2024-08-03 224028](https://github.com/user-attachments/assets/993aabec-32e2-4d96-80c0-2961d54b5d1b)

*Ref 2: Network Diagram*


Configure each access point by changing the SSID Name and authentication.

![Screenshot 2024-08-04 121433](https://github.com/user-attachments/assets/a85dbdc9-255c-4235-8536-9f1329f75f57)


*Ref 3: Network Diagram*

Configure the with the VLAN's and IP address and enabling DHCP

![Screenshot 2024-08-04 124321](https://github.com/user-attachments/assets/9fddf32e-f8c1-4c99-8854-134ed5470c94)

*Ref 4: Network Diagram*

![Screenshot 2024-08-04 130705](https://github.com/user-attachments/assets/8723a97c-b577-4adc-9808-d1a35064f7c6)

*Ref 5: Network Diagram*

![Screenshot 2024-08-04 130812](https://github.com/user-attachments/assets/397dbc29-bde9-45b3-8ca1-6bd1ca3f77ed)

*Ref 6: Network Diagram*

This command will enable DHCP service "service dhcp" and enable the folling CLI commands below for the 3 departments

![Screenshot 2024-08-04 181240](https://github.com/user-attachments/assets/b72b5b68-8f27-41c3-b60f-8a4eb8541339)

*Ref 7: Network Diagram*

Add 2 more device i.e a laptop and a smartphone on all 3 department and try to confirm if they all have access to the internet and have been assigned an IP address.

![Screenshot 2024-08-04 183735](https://github.com/user-attachments/assets/83132009-f034-491b-a9b0-1d8dc1131505)

*Ref 8: Network Diagram*

This showed that the 2 devices added to each department was connected successuflly using the Access Point for each departments.
