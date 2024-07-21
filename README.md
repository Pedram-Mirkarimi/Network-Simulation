# Network-Simulation

![image](https://github.com/user-attachments/assets/3c4cbe25-960b-4076-acc7-bbaff61af4d4)
"Figure 01 – Overview of the simulation"


The process of finding the right way to transfer data in a network or from one network to another is called routing. Routers perform routing in two ways, which are:
1) static routing
2) dynamic routing

In this project, it is intended to talk about static routing. At first, the simulation that has three separate networks is displayed with a picture.

![image](https://github.com/user-attachments/assets/3c6e5d85-351a-4113-95b5-780f6b587ae4)
"Figure 02 – Network number one"

![image](https://github.com/user-attachments/assets/50e26ea2-6c96-43bb-99e1-05c6867d7ff9)
"Figure 03 - Network number two"


Network 1 & 2 Components:
1. PC
2. Switch 2960
3. Straight Cable

The only thing that distinguishes two networks (network one and two) is their IP.
The range of IP networks is as follows:
-Network one: 192.168.1.0
-Network two: 172.16.1.0

A network can have various devices such as: computer, laptop, printer, server, etc., in this project, the existence of a PC is sufficient for data transfer.

In networks one and two, at first, the computers are connected to the switch with a straight cable, then the PCs are given IPs based on their existence in a different network.

![image](https://github.com/user-attachments/assets/1fa98e4f-9663-4513-a0e1-281094531e54)
"Figure 04 – IP of PC1 in network one"

![image](https://github.com/user-attachments/assets/8592b559-c25a-479f-af78-395658ec575e)
"Figure 05 – IP of PC2 in network two"
*Of course, it should be noted that PC1's IP is class "C" and PC2's IP is class "B".

Normally, the devices in each network can communicate with each other with only one IP address, but because the purpose of this project is the fixed routing of routers, we are satisfied with one PC in each network.
The point is that if a network wants to send data from its network to another network with a different IP address, in this section we need routers, and since routing must be done, in this project we We need two routers that create an independent network by themselves.


![image](https://github.com/user-attachments/assets/fe8f2893-7ca8-4f86-807d-4d37a9904aec)
"Figure 06 - Network number 3"

Network number 3 Components:
1. Router 2911
2. Cross-Over Cable

Routers, unlike switches, are initially turned off and must be turned on, and then we assign an IP to that router, which must be assigned as the Default Gateway to all connected devices in the desired network.


![image](https://github.com/user-attachments/assets/aae7f777-a002-4a26-abe8-55ebba264dcf)
"Figure 07 – 0/0 port settings of Router 1"

As mentioned earlier Router1 is assigned a static IP.

![image](https://github.com/user-attachments/assets/1a9a5201-cfdd-48a5-9c88-e1755aa33900)
"Figure 08 - Setting the default gateway feature"


Because there is only one device (PC) in network one, we set the IP address of the router (port 0/0) to the default gateway feature of the device.
Then we set the above operation on network two and Router2.

![image](https://github.com/user-attachments/assets/b9662d15-f765-47ee-a2e4-27fbadc4cfa7)
"Figure 09 – 0/0 port settings of Router 2"

![image](https://github.com/user-attachments/assets/2cc6f5ac-ae8f-43e6-aa45-3487eb0aaef4)
"Figure 10 - Setting the default gateway feature"

Now the work with networks one and two is finished and we need to make settings to establish Router1 and Router2 in network three.


Its first configuration is to assign a Network ID but with different IPs for two routers.
We consider the network ID as 1.1.1.0 and set different IP routers according to the ID.

![image](https://github.com/user-attachments/assets/1b1d218b-69e8-4c99-900f-ded31c0a51e7)
"Figure 11 – Set an IP on port 0/1 of Router 1"

![image](https://github.com/user-attachments/assets/90171c8e-b50d-4eab-acfc-d779c79c604e)
"Figure 12 – Set an IP on port 0/1 of Router 2"


After setting the IPs of the routers for the third network, it is time for the last operation to assign a fixed route to the routers.

![image](https://github.com/user-attachments/assets/95c8e07d-6379-43b8-a280-0738be85d2c2)
"Figure 13 – Router1 static routing setup"

![image](https://github.com/user-attachments/assets/c3599ab8-355e-4d73-95aa-9fe49b005bfe)
"Figure 14 – Router2 static routing setup"


In images 13 and 14, we enter the Routing section and then Static, and to determine a route, we must determine 3 features, which are:
-Network: The address of the network to which the information is to be sent.
-Mask: Depending on the type of network address, we enter the mask.
-Next Hop: Determining the path through which we can access the desired network.

The settings are finished and we will see the result together in the following section.


![image](https://github.com/user-attachments/assets/5f4b8bc7-7483-4496-9021-01ca13048234)
"Figure 15 - The result of sending and receiving information to each other"
