# VTP-VLAN-Trunking-Protocol-


### Lab Topology

<div>
  <img width="850" height="603" alt="image" src="https://github.com/user-attachments/assets/c954aad0-c103-4db0-871e-4c2ee9e2ba29" />
</div>


### Objective

In this lab, we will create VLANs on the VTP Server switch and observe how those VLANs are automatically propagated to the VTP Client switches.

We will also examine the behavior of a VTP Transparent switch, which forwards VTP advertisements to neighboring switches but does not synchronize or apply VLAN information received from the VTP domain.

Finally, we will add a new switch to the network, configure the VTP domain name and password, and set its VTP mode to Client. We will then create additional VLANs on this switch to increase its configuration revision number beyond that of the existing VTP Server. This demonstration will show how a switch with a higher VTP revision number can overwrite the VLAN database of other switches in the same VTP domain, potentially deleting existing VLANs and replacing them with its own VLAN configuration.

### First, configure interfaces Fa0/1 and Fa0/2 on the VTP Server switch as trunk ports to allow VLAN traffic to be carried between switches.

<div>
  <img width="395" height="41" alt="image" src="https://github.com/user-attachments/assets/eed185c6-ee49-46a9-b2c6-39955773173f" />
</div>

<div>
  <img width="647" height="250" alt="image" src="https://github.com/user-attachments/assets/ae5e15d2-a867-4105-be26-cb48d2dd4f8e" />
</div>

### Next, configure the corresponding interfaces on all VTP Client and VTP Transparent switches as trunk ports to ensure VLAN traffic and VTP advertisements can be exchanged throughout the network.

<div>
  <img width="628" height="236" alt="image" src="https://github.com/user-attachments/assets/3e1ec8cc-44fc-4990-a5ba-2f6704cecd35" />
</div>


<div>
  <img width="644" height="285" alt="image" src="https://github.com/user-attachments/assets/d0610ada-2f0f-4e85-87f7-3a8347c8a07d" />
</div>

### Show VTP status from the server

<div>
  <img width="636" height="264" alt="image" src="https://github.com/user-attachments/assets/620db32b-116e-46b9-bd0a-009b3688adde" />
</div>


### Create VLANs, configure the VTP domain, password, and Server mode on the VTP Server switch.

- Create VLANS
  
<div>
  <img width="552" height="152" alt="image" src="https://github.com/user-attachments/assets/82fa1e84-bc3a-4c2c-9115-82d2063130f1" />
</div>

  - Configure doamin
  - configure password
  - set the server mode
    
<div>
  <img width="558" height="241" alt="image" src="https://github.com/user-attachments/assets/f6d6d102-66d2-42b4-9e0b-d92a12d1a1e2" />
</div>

### Show VTP status result after config

<div>
  <img width="604" height="262" alt="image" src="https://github.com/user-attachments/assets/04297e9a-658d-4292-bc2b-8e47993e6da6" />
</div>

<div>
  <img width="635" height="251" alt="image" src="https://github.com/user-attachments/assets/c9cc7c55-0715-49b3-9307-944f58f0c885" />
</div>

### On the Client switch

### VTP status on the client

<div>
  <img width="563" height="251" alt="image" src="https://github.com/user-attachments/assets/865004ba-f6e9-4a0e-9c3d-533bb59a56ec" />
</div>

password and mode

<div>
  <img width="607" height="151" alt="image" src="https://github.com/user-attachments/assets/e46a3ffb-70b3-4d21-b504-b818614aa209" />
</div>

<div>
  <img width="600" height="249" alt="image" src="https://github.com/user-attachments/assets/81865519-59f0-4a72-9358-44149d7f3e74" />
</div>

### vtp status result on the transparent switch

<div>
  <img width="1016" height="720" alt="image" src="https://github.com/user-attachments/assets/61fc2730-530b-491c-b859-a981d085d311" />
</div>

## No Vlans reflected

<div>
  <img width="637" height="211" alt="image" src="https://github.com/user-attachments/assets/ff02cef2-71f6-489a-870d-38285b5da0c4" />
</div>


### We add a new switch and create multi other VLANS on it, its configuration revision increases to 4

<div>
  <img width="626" height="490" alt="image" src="https://github.com/user-attachments/assets/56f1c643-4a61-42c6-a38a-2a9c06fc4154" />
</div>
