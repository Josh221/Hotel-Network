# Design and Implementation of an enterprise network for a hotel.

## Networking simulation software used:

Cisco Packet Tracer 8.2.2

## Scenario & Requirements:

You are required to design and implement the Vic Modern Hotel network. The hotel has three floors; on the first floor there are three departments (Reception, store and Logistics), in the second floor there are three departments (Finance, HR and Sales/Marketing), while the third floor hosts IT and Admin. Therefore, the following are part of the considerations during the design and implementation:

•	There should be three routers connecting each floor (all placed in the server room in IT department).

•	All routers should be connected to each other using serial DCE cables.

•	The network between the routers should be 10.10.10.0/30,10.10.10.4/30 and 10.10.10.8/30.

•	Each floor is expected to have one switch (placed on the respective floor).

•	Each floor is expected to have WIFI networks connected to laptops and phones.

•	Each department is expected to have a printer.

•	Each department is expected to be in a different VLAN with the following details:


1st Floor:

- Reception- VLAN 80, Network of 192.168.8.0/24
  
- Store- VLAN 70, Network of 192.168.7.0/24
  
- Logistics- VLAN 60, Network of 192.168.6.0/24
  
2nd Floor:

- Finance- VLAN 50, Network of 192.168.5.0/24
  
- HR- VLAN 40, Network of 192.168.4.0/24
  
- Sales- VLAN 30, Network of 192.168.3.0/24
  
3rd Floor:

- Admin- VLAN 20, Network of 192.168.2.0/24
  
- IT- VLAN 10, Network of 192.168.1.0/24
  

•	Use OSPF as the routing protocol to advertise routes.

•	All network devices are expected to dynamically obtain IP addresses with their respective router configured as the DHCP server.

•	All the devices in the network are expected to communicate with each other.

•	Configure SSH in all the routers for remote login.

•	In IT department, add PC called Test-PC to port fa0/1 and use it to test remote login.

•	Configure port security to IT-dept switch to allow only Test-PC to access port fa0/1 (use sticky method to obtain mac-address with violation mode of shutdown.)

## Technologies Implemented:
1.	Creating a network topology using Cisco Packet Tracer.
   
3.	Hierarchical Network Design.
   
5.	Connecting Networking devices with Correct cabling.
   
7.	Creating VLANs and assigning ports VLAN numbers.
   
9.	Subnetting and IP Addressing.
    
11.	Configuring Inter-VLAN Routing (Router on a stick).
    
13.	Configuring DHCP Server (Router as the DHCP Server).
    
15.	Configuring SSH for secure Remote access.
    
17.	Configuring switchport security or Port-Security on the switches.
    
19.	Configuring WLAN or wireless network (Cisco Access Point).
    
21.	Host Device Configurations.
    
23.	Test and Verifying Network Communication.

## Network Layout:

![image](https://github.com/user-attachments/assets/d9eb4f68-bc73-49a1-951f-75c084b1d07d)

## Configuration:

Turning on all necessary ports for all 3 routers:

Router 1

![image](https://github.com/user-attachments/assets/6705390c-2021-4e3e-9474-dbf9f4145efc)

Router 2

![image](https://github.com/user-attachments/assets/241af95c-edea-4620-9dda-0250b4da93a2)

Router 3

![image](https://github.com/user-attachments/assets/3f5bd4eb-8698-43f0-887b-5397214301fb)

Setting clock rates for serial DC interface on each router:

Router 1

![image](https://github.com/user-attachments/assets/d2cb4822-c239-4eab-b63a-6dee31653359)

Router 2

![image](https://github.com/user-attachments/assets/21fa587f-a74a-42c2-a617-98126ea4eca9)

Router 3

![image](https://github.com/user-attachments/assets/8985ac84-7620-40e4-a8f7-784e42c38432)

Configuring VLANS & trunk for each switch:

1st-floor switch

![image](https://github.com/user-attachments/assets/2cabb6e3-941c-4117-88f5-ac3d457f1592)
![image](https://github.com/user-attachments/assets/7c13b58a-d2f2-4fa8-9dbb-ea26b9fa80fc)

2nd-floor switch

![image](https://github.com/user-attachments/assets/ce974157-0b5b-4473-b187-d76e5499e541)

3rd-floor switch

![image](https://github.com/user-attachments/assets/cde164ef-a39b-4abc-9d2b-a9b7cb65e5b3)

Configuring router IP addresses:

Router 1

![image](https://github.com/user-attachments/assets/d38df510-071a-4ea3-9676-27439f0fa61e)

Router 2

![image](https://github.com/user-attachments/assets/0aa7656d-5f7a-4bc8-a675-0f20115a5ab6)

Router 3

![image](https://github.com/user-attachments/assets/de4ae862-7208-421b-bd62-7d091d5d3aac)

Creating sub-interfaces for each VLAN on all 3 routers:

Router 1

![image](https://github.com/user-attachments/assets/392596c2-b0ca-4ea5-8e59-01687f2d1d10)

Router 2

![image](https://github.com/user-attachments/assets/6b2bae1a-7dd3-40b5-a536-ca9d0cbcb936)

Router 3

![image](https://github.com/user-attachments/assets/87317f62-9413-4022-977d-55b614936a99)

Creating DHCP pools on each router:

Router 1

![image](https://github.com/user-attachments/assets/511e00ef-5a4a-47f8-aafb-e00bb8e789b7)

Router 2

![image](https://github.com/user-attachments/assets/e826f156-ebd0-4ebe-848e-63212aae0daa)

Router 3

![image](https://github.com/user-attachments/assets/6be8a2e6-4b6e-423d-8595-9920063a60f8)

Configuring OSPF on all 3 routers:

Router 1

![image](https://github.com/user-attachments/assets/d016c5d9-f445-44c3-a28c-8e1b4fa06300)

Router 2

![image](https://github.com/user-attachments/assets/31362893-d279-4689-bc93-23eb14ad0eaf)

Router 3

![image](https://github.com/user-attachments/assets/a63b8968-6800-4825-a856-a806ed1394f8)

Configuring the access points for each floor:

Floor 1

![image](https://github.com/user-attachments/assets/7c8b7bc8-cca0-40c7-b5ff-19d742074f80)

Floor 2

![image](https://github.com/user-attachments/assets/cea6ac64-1b3b-4a57-84cd-455646285c90)

Floor 3

![image](https://github.com/user-attachments/assets/52df657e-310e-4d62-a9d0-1092abd1bbac)


Configuring SSH on routers for remote login:

Router 1

![image](https://github.com/user-attachments/assets/dda7d5ba-19f6-4f59-ba75-8233514c809f)

Router 2

![image](https://github.com/user-attachments/assets/a86fd32b-b2e7-478e-bef1-0f1d02d1ec10)

Router 3

![image](https://github.com/user-attachments/assets/8ec2e832-e6d1-4b91-a968-7c571c069db8)

Testing ssh from a PC to different routers:

![image](https://github.com/user-attachments/assets/68ab6717-45d3-4b8c-b1a6-9d1ee448d754)

Configuring port security for the IT test PC:

![image](https://github.com/user-attachments/assets/1900db05-47e1-4de0-9b8b-161cf52d2c35)

![image](https://github.com/user-attachments/assets/45ab61f7-379a-48ca-a749-d3630f3c71eb)

Testing connection from IT PC to the marketing printer:

![image](https://github.com/user-attachments/assets/7c5fbe80-69d8-4425-ac55-3b9041ec4d21)

## Final Network Layout:
![image](https://github.com/user-attachments/assets/741c8fe7-b9e4-46ab-a1a7-c8b8e50029f4)

