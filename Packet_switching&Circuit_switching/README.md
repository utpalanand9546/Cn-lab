# Lab Assignment 2: Packet Switching and Circuit Switching

---

## Description

This assignment demonstrates the working of packet switching and circuit switching using Cisco Packet Tracer. The behavior of data transmission is observed by comparing single packet communication with continuous communication between devices.

---

## Steps to Perform the Experiment

### Packet Switching

1. Create a network with:

   * 2 PCs
   * 2 Switches
   * 1 Router

2. Connect devices:

   * PC → Switch → Router → Switch → PC

3. Configure IP addresses:

   * PC1 → 192.168.1.2
   * PC2 → 192.168.2.2

4. Configure router interfaces:

   * FastEthernet0/0 → 192.168.1.1
   * FastEthernet1/0 → 192.168.2.1

5. Set default gateways:

   * PC1 → 192.168.1.1
   * PC2 → 192.168.2.1

6. Send packet using Add Simple PDU

7. Observe packet flow in Simulation Mode

---

### Circuit Switching (Simulation)

1. Use the same network topology

2. Send multiple packets:

   * Use Add Simple PDU multiple times
   * Or repeat ping between devices

3. Observe continuous packet flow

4. Use Simulation Mode to analyze communication

---

## Learnings

* Packet switching transmits data in individual packets
* Circuit switching maintains continuous communication between devices
* Packet switching is flexible and efficient
* Circuit switching provides stable transmission
* Continuous packet flow can simulate circuit switching in Packet Tracer

---

## Files Included

* Packet Tracer file (.pkt)
* Screenshots of packet switching and circuit switching
* README documentation

---
