# DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-

When two notes are trying to communicate, they may use a THREE WAY HANDSHAKE, the actor will be using a target and attacking machine, the attacking machine will be sending a SYN packet and if the packet goes to the target machine, the target machine will reply with an acknowledgement (SYN/ACK) packet. After that the target machine will be waiting to get the final package from source again which will be ACK packets. The actor will load the target machine with many task and with that it will cause DoS. 
Metaspoilt in kali VM will be used as the attacking maching while centos will be used as the target machine.


STEP 1: Scaning  server for open port using the following command “sudo -sS nmap 172.16.0.3”. The screenshot below shows the open port (8021) indicated with red arrow which can be a suitable target.![image](https://github.com/Mirian02/DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-/assets/118598344/efbb6f81-7cbc-4947-bc50-0e0d6840b252)

STEP 2: In kali, metaspoilt was utilized by the actor to carry out the DoS attack. Metaspoilt has this auxiliary called SynFlood, the actor will be using that SynFlood to attack the target machine. In other to run metaspoilt “sudo msfconsole” command is used, after using “pwd” to locate the file folder. From the below screenshot (highlighted in yellow), it shows Metaspoilt has about 1062 auxxiliary and the actor is looking for the one which is “SynFlood”.![image](https://github.com/Mirian02/DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-/assets/118598344/c80be7cd-f831-4d4c-9129-cbadbe65aa23)

STEP 3: command “search synflood” is used to search for the location of the exact auxiliary needed. Below screenshots displays the location.![image](https://github.com/Mirian02/DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-/assets/118598344/88551aa9-9acc-46ad-8d94-c6a745286593)

STEP 4: The screenshots below “shows options” of the interface (a name can be given to the interface machine but it is not required), number ( the actor can have numbers of the packet which is being sent but is not required), RHOST (R host is the remote host (victim machine), the host needs to be set to the location the actor wants to attack), from the diagram the remote port has picked up 80 by default but the hacker will be using port 8021 which was seen earlier when checking for open port and the SHOST which will be the ip address of the attacker machine (host machine). <img width="379" alt="image" src="https://github.com/Mirian02/DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-/assets/118598344/4becde3f-0d2a-4f63-880c-baf806509333">

STEP 5: Setting the target remote HOST (windows), remote PORT, Spoof IP address and show options.<img width="356" alt="image" src="https://github.com/Mirian02/DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-/assets/118598344/30fd9077-247f-4209-90e7-42d294f3c0ac">

STEP 6: Command “exploit” to recieve traffic, below screenshots shows the SYN flooding. ![image](https://github.com/Mirian02/DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-/assets/118598344/ac23ba33-fae9-4517-aa84-c4d2c332efee)

Step 7: the actor loads Wireshark in other to see the amount of traffic is receiving from the target machine as shown in the below screenshot. <img width="468" alt="image" src="https://github.com/Mirian02/DENIAL-OF-SERVICE-Using-SynFlood-ATTACK-/assets/118598344/367ac66f-eb07-4808-ada4-1d8625599dfa">


