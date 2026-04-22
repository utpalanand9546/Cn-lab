# Packet Flow Visualization Using Simulation Mode

## Project Overview
[cite_start]This project focuses on visualizing how data packets move through a network using **Cisco Packet Tracer’s Simulation Mode**[cite: 1, 3]. [cite_start]By building a simple Local Area Network (LAN), we observe the step-by-step process of devices communicating, how switches manage traffic, and the specific behavior of key networking protocols like **ARP** and **ICMP**[cite: 3, 33, 46].

---

## Experiment Objectives
* [cite_start]Use Simulation Mode to visualize packet movement step-by-step[cite: 3, 33].
* [cite_start]Understand how switches learn and store **MAC addresses**[cite: 3, 22].
* [cite_start]Observe the interaction between **ICMP** (Ping) and **ARP** (Address Resolution)[cite: 3, 34].
* [cite_start]Compare the efficiency of a first-time communication vs. subsequent communications[cite: 37].

## Components Used
* [cite_start]**Software:** Cisco Packet Tracer[cite: 5, 47].
* [cite_start]**Switch:** 1x Cisco 2960[cite: 6, 49].
* [cite_start]**End Devices:** 3x PCs (PC0, PC1, PC2)[cite: 7, 50].
* [cite_start]**Cabling:** Copper Straight-Through cables[cite: 8, 51].

---

## Core Networking Concepts

### ICMP (Internet Control Message Protocol)
[cite_start]ICMP is primarily used for connectivity testing[cite: 12, 13].
* [cite_start]**Echo Request:** Sent by the source device to the destination[cite: 14].
* [cite_start]**Echo Reply:** Sent by the destination back to the source to confirm connectivity[cite: 15].

### ARP (Address Resolution Protocol)
[cite_start]ARP maps an IP address to a physical MAC address[cite: 16, 17].
* [cite_start]Before sending data, a source must know the destination's MAC address[cite: 18, 19].
* [cite_start]If unknown, an **ARP Request** is broadcast to all devices[cite: 20].
* [cite_start]The target device responds with an **ARP Reply** (unicast)[cite: 21].

### Switch Behavior & MAC Learning
[cite_start]A switch works at the **Data Link Layer** and manages traffic using a MAC address table[cite: 23, 26].
* [cite_start]**Learning:** The switch records the source MAC address of incoming frames[cite: 24, 25].
* [cite_start]**Forwarding:** If the destination MAC is unknown, the switch broadcasts the data to all ports[cite: 27, 28]. [cite_start]Once known, it sends data only to the specific destination port[cite: 29, 30].

---

## Methodology & Tasks

### Task 1: Building the LAN
[cite_start]A simple topology was created by connecting PC0, PC1, and PC2 to the 2960 Switch[cite: 52, 53, 54]. [cite_start]IP addresses were assigned to each PC to allow logical communication[cite: 55].

### Task 2: First Ping Observation
[cite_start]Initiated a ping from **PC0 to PC1** in Simulation Mode[cite: 60, 61].
* [cite_start]**Flow:** PC0 sends an **ARP Request** (Broadcast) because it does not yet know PC1's MAC address[cite: 63, 64].
* [cite_start]**Switch Action:** The switch learns PC0’s MAC and forwards the broadcast to all devices[cite: 67, 68].
* [cite_start]**Resolution:** PC1 replies with its MAC address[cite: 69, 70].
* [cite_start]**Communication:** Only after ARP is resolved does the **ICMP Echo Request** and **Reply** take place[cite: 72, 74].

### Task 3: Second Ping Observation
[cite_start]Repeating the ping between PC0 and PC1[cite: 76, 77].
* [cite_start]**Change:** No ARP request is sent this time[cite: 79].
* [cite_start]**Reason:** The MAC address is already stored in the PC’s ARP cache[cite: 81, 82].
* [cite_start]**Result:** Communication is faster and involves only ICMP packets[cite: 43, 44, 80].

### Task 4: MAC Table Verification
[cite_start]Accessing the Switch CLI to confirm the learned addresses[cite: 83, 84, 85].
* [cite_start]**Command:** `show mac address-table`[cite: 88].
* [cite_start]**Observation:** The table correctly lists the MAC addresses of the connected PCs mapped to their respective ports[cite: 88].

---

## Conclusion
[cite_start]This experiment successfully demonstrates that network communication involves multiple layers[cite: 36]. [cite_start]Simulation Mode highlights how ARP overhead affects initial communication and how switches optimize local traffic by learning device hardware addresses[cite: 34, 37, 38].
