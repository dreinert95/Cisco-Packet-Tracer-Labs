# Cisco-Packet-Tracer-Labs
This repository features a collection of hands-on Cisco Packet Tracer projects that reflect my growth, skills, and practical experience as I progress on my journey to becoming a network engineer.

# ALL OF THESE LABS BELONG TO JEREMY'S IT LAB. THESE ARE LABS THAT I HAVE FOLLOWED ALONG WITH FROM HIS YOUTUBE VIDEOS THAT CAN BE FOUND HERE --> https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbnZ1M1NhUXp3QkdZaGF4dnFDYkRONm91ck1XZ3xBQ3Jtc0tscFAwbVBBWnhNQW0tZ0RQMHNGZ2pzQWE2TG1UazZsdnFSbWZLWnJQTGJHdmIwN1NaRnNiNF8wcWxMNnloa2c4OW9kbXdBeGdBbW43d3dUREowRkhJUnhIOTJZR0RBZUhRWlBQb3JmQ2JlUU51a19Ddw&q=https%3A%2F%2Fjitl.jp%2Fccna-files&v=H8W9oMNSuwo

# Lab 1
**Devices used:**

Cisco 2911 routers (x2)

Cisco 2960 switches (x2)

Cisco 5505 Firewalls (x2)

PCs (x2)

Servers (x2)

Laptop (Attacker)


**Objective:** Connect the devices together using Auto Choose Connection Type function.

**Place Devices:**

1. Select "Network Devices" --> Routers --> 2911 (x2)
2. Select "Network Devices" --> Switches --> 2960 (x2)
3. Select "Network Devices" --> Security --> 5505 (x2)

   *The New York Branch has the firewall placed between R1 and The Internet. The Tokyo Branch has the firewall placed between R2 and       SW2
5. Select "End Devices" --> PC (x2 in New York branch)
6. Select "End Devices" --> Server (x2 in Tokyo branch)
7. Select "End Devices" --> Laptop (in the middle below The Internet)

**Connect Devices:**

1. Select "Connections" --> Automatically Choose Connection Type

   *Click on PC1 then SW1
2. Select "Connections" --> Automatically Choose Connection Type

   *Click on PC2 then SW1
3. Hold down Control and select "Automatically Choose Connection Type"

   *Connect SW1 to R1
   
   *Connect R1 to FW1
   
   *Connect FW1 to The Internet
   
   *Connect The Internet to R2
   
   *Connect R2 to FW2
   
   *Connect FW2 to SW2
   
   *Connect SW2 to SRV1
   
   *Connect SW2 to SRV2
   
   *Connect Attacker to The Internet
   
4. Click "Cancel" on "Automatically Choose Connection Type"

# Lab 2

**Objective:** Connect the network devices together according to the labels. Use the appropriate type of cable. For practice, assume that Auto MDI-X is disabled or not supported.

*Note - Packet Tracer does not differeniate between single-mode and multi-mode fiber. But think about which one is appropriate when you use a fiber connection.

**Cables used:**

copper straight-through

copper cross-over

fiber connections

**Connect Devices:**

1. PCs transmit data on pins 1 and 2, and receive data on pins 3 and 6
2. Switches transmit data on pins 3 and 6, and receive data on pins 1 and 2

   *Therefore,we can use a straigh-through cable to connect all of the PCs, as well as SRV1 to the switches

3. Select "Connections" --> Copper Straight-Through

   *Connect PC1 to SW3. Connect the FastEthernet0 interface on the PC (which is the PC's network interface         card) to any of the FastEthernet interfaces on the switch

   *Connect PC2 to SW4

   *Connect PC3 to SW7

   *Connect SRV1 to SW8

4. Connect the switches together

   *Devices of the same type require crossover cable. Otherwise the transmit pins will be connected to the         transmist pins, and the receive pins will beconnected to the receive pins. This will not allow data to be      sent successfully between the devices.

   *Connect SW3 to SW1

   *Connect SW1 to SW2

   *Connect SW2 to SW4

   *Connect SW7 to SW5

   *Connect SW5 to SW6

   *Connect SW8 to SW6

5. Connect the switches to the routers

   *Routers are like PCs. They transmit data on pins 1 and 2, and receive data on pins 3 and 6. Therefore, we will use a straight-through cable to connect the switches to the routers.

   *Connect SW1 to R2

   *Connect SW2 to R2

   *Connect SW5 to R4

   *Connect SW6 to R4

6. Connect the routers

   *Since they are the same device type, we must use a crossover      cable. **Note the distances**

   *R1 and R2 are 50 meters apart, therefore we can use copper cabling (which permits distances up to 100 meters)

   *Connect R2 to R1

   *R1 and R3 are 3 kilometers apart, therefore we must use a fiber-optic cable (single-mode permits distances of 100+ kilometers. multi-mode permits distances of 550 meters)

   *R3 and R4 are 250 meters apart. This distance is too far for a UTP cable, but not so long that we need single-mode fiber. Therefore, we will use a multi-mode fiber cable.


# Lab 3

**Objective:** 
  
  Examine network traffic using packet tracer's 'simulation mode'

  Identify which layers of the OSI Model are being used

  Release and renew PC1's IP address to generate some Layer 7 traffic. Then analyze the traffic with simulation mode.

**Devices:**

Cisco 2911 routers (x2)

Cisco 2960 switches (x2)

Server (x1)

PC (x1)

**Network Interfaces:**

G0/0

G0/1

G0/2

F0/1

"G" - gigabit ethernet. these interfaces operate at a speed of one gigabit per second

"F" - fastethernet. these interfaces operate at 100 megabits per second

**Network Addresses:**

192.168.1.0/24

10.0.0.0/24

# routers are used to connect different networks. there are two networks displayed in the lab diagram

  *Network Address 192.168.1.0/24 --> SRV1, PC1, SW1, SW2 and R1's G0/0 interface
  
  *SRV1 '.100' means that its IP address is 192.168.1.100
  
  *R1 '.1' means that its IP address is 192.168.1.1

  *Network Address 10.0.0.0/24 --> R1's G0/1 interface and R2's G0/0 interface
  
  *R1 '.1' means that its IP address is 10.0.0.1
  
  *R2 '.1.' means that its IP address is 10.0.0.2

**Simulation mode:**

*Activate 'Simulation mode' in the bottom right-hand corner with the 'Simulation' button

*Utilize the 'Play Controls' to see various network traffic being sent around

**Network Traffic Analysis via Simulation Panel:**

*At Device 2 means that SW2 is the one sending out the data

*Type STP - STP is the Spanning-Tree Protocol (Layer 2)

*Out Layers:
  
  Layer 2: IEEE 802.3 Header 0001.C70E.BD19>>0180.C200.0000 LLC STP BPDU

    *IEEE 802.3 is the standard number for Ethernet. Therefore this is an Ethernet Layer 2 Header

  Layer 1: Port(s): FastEthernet0/1 GigabitEthernet0/1

    *The information is the two interfaces that it sends the frame out of.

    *Information like the physical ports, or interfaces, on a device are Layer 1 information because it is the physical layer

*At Device R1

*Type OSPF (Open Shortest Path First) - used to discover the best paths to different networks (Layer 3)
*STP only had Layer 2 and Layer 1 information. OSPF has Layer 3, Layer 2 and Layer 1 information

*Out Layers:

  Layer 3: IP Header Src. IP: 192.168.1.1, Dest. IP: 224.0.05 OSPF HELLO

*PC1 - using a protocol called DHCP to automatically receive an IP address

  *DHCP (Dynamic Host Configuration Protocol) - a network protocol used to automate the configuration of devices on IP networks
  *DHCP is a Layer 7 protocol

  *Release PC1's current IP address and then renew it

  *Click on PC1

  *Click on 'Desktop'

  *Click on 'Command Prompt' --> this functions like a windows command prompt

  *type 'ipconfig' to view the current IP address

  *type 'ipconfig /release' to release the current IP address

  *type 'ipconfig /renew' to renew the IP address

  *You will see information all the way up to Layer 7, except Layers 5 and 6. This is because in the TCP/IP model (the model actually in use) Layers 5, 6 and 7 are all combined into a single layer called the Application Layer. Therefore, you will not see any Layer 5 or Layer 6 information, but you can consider it to be part of the Layer 7 information.

# Lab 4 - Basic Device Security

This lab will be hands on in the Cisco IOS CLI (Command Line Interface)
