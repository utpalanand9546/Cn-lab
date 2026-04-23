# Lab Assignment 7: Sliding Window Protocol with Piggybacking

---

## Description

This assignment demonstrates the concept of sliding window protocol with piggybacking using Cisco Packet Tracer. Piggybacking improves communication efficiency by combining acknowledgment with outgoing data instead of sending it separately.

---

## Steps to Perform the Experiment

1. Create a network with:

   * 2 PCs
   * 1 Switch

2. Connect both PCs to the switch

3. Assign IP addresses:

   * PC1 → 192.168.70.1
   * PC2 → 192.168.70.2

4. Switch to Simulation Mode

5. Apply filters:

   * TCP
   * ICMP (optional)

6. Generate traffic in both directions:

   * Send PDU from PC1 → PC2
   * Send PDU from PC2 → PC1

7. Run the simulation

8. Click on packets and open:

   * Outbound PDU Details
   * Inbound PDU Details

9. Observe:

   * Acknowledgment (ACK) field
   * Data transmission

---

## Observation

* Packets contain both data and acknowledgment
* ACK is not sent separately
* Communication is bidirectional

---

## Concept of Piggybacking

Piggybacking is a technique in which the acknowledgment is combined with outgoing data in the same packet. This reduces the number of packets transmitted and improves network efficiency.

---

## Learnings

* Piggybacking reduces network overhead
* TCP supports piggybacking
* Bidirectional communication is required
* Simulation mode helps analyze packet details

---

## Files Included

* Packet Tracer file (.pkt)
* Screenshots of simulation
* README documentation

---
