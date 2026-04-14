# Cisco-Packet-Tracer-Labs
This repository features a collection of hands-on Cisco Packet Tracer projects that reflect my growth, skills, and practical experience as I progress on my journey to becoming a network engineer.

# ALL OF THESE LABS BELONG TO JEREMY'S IT LAB. THESE ARE LABS THAT I HAVE FOLLOWED ALONG WITH FROM HIS YOUTUBE VIDEOS THAT CAN BE FOUND HERE --> https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbnZ1M1NhUXp3QkdZaGF4dnFDYkRONm91ck1XZ3xBQ3Jtc0tscFAwbVBBWnhNQW0tZ0RQMHNGZ2pzQWE2TG1UazZsdnFSbWZLWnJQTGJHdmIwN1NaRnNiNF8wcWxMNnloa2c4OW9kbXdBeGdBbW43d3dUREowRkhJUnhIOTJZR0RBZUhRWlBQb3JmQ2JlUU51a19Ddw&q=https%3A%2F%2Fjitl.jp%2Fccna-files&v=H8W9oMNSuwo

# Lab 1
Devices Used:

Cisco 2911 routers (x2)
Cisco 2960 switches (x2)
Cisco 5505 Firewalls (x2)
PCs (x2)
Servers (x2)
Laptop (Attacker)

Objective: Connect the devices together using Auto Choose Connection Type function.

Place Devices:

1. Select "Network Devices" --> Routers --> 2911 (x2)
2. Select "Network Devices" --> Switches --> 2960 (x2)
3. Select "Network Devices" --> Security --> 5505 (x2)

   *The New York Branch has the firewall placed between R1 and The Internet. The Tokyo Branch has the firewall placed between R2 and       SW2
5. Select "End Devices" --> PC (x2 in New York branch)
6. Select "End Devices" --> Server (x2 in Tokyo branch)
7. Select "End Devices" --> Laptop (in the middle below The Internet)

Connect Devices:

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
