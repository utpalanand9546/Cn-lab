# Transmission Failure Demonstration (Link Errors & Retransmission)

## Project Overview
[cite_start]This project demonstrates how communication errors occur in a computer network by intentionally forcing link failures[cite: 379, 381]. [cite_start]Using **Cisco Packet Tracer’s Simulation Mode**, we observe how a network responds when physical links are interrupted and how it recovers once the connection is restored[cite: 381, 393].

---

## Experiment Objectives
* [cite_start]Demonstrate the impact of physical link failure on data transmission[cite: 381, 388].
* [cite_start]Observe and interpret error messages like "Request timed out" in real-time[cite: 381, 397].
* [cite_start]Understand how networks resume communication after a link is recovered[cite: 381, 393].

## Technical Requirements
* [cite_start]**Software:** Cisco Packet Tracer[cite: 383].
* [cite_start]**Switch:** 1x Cisco 2960[cite: 384].
* [cite_start]**End Devices:** 2x PCs (PC0, PC1)[cite: 385].
* [cite_start]**Cabling:** Copper Straight-Through cables[cite: 386].

---

## Key Networking Concepts

### 1. Physical Link Dependability
[cite_start]Communication relies entirely on stable physical connections (cables)[cite: 387]. [cite_start]If a cable is disconnected, the flow of data is immediately interrupted, leading to[cite: 388]:
* [cite_start]**Packet Loss:** Data fails to reach its intended destination[cite: 390].
* [cite_start]**Timeouts:** The source device stops waiting for a response that will never arrive[cite: 391].
* [cite_start]**Communication Failure:** The established session between devices is broken[cite: 392].

### 2. ICMP Behavior During Errors
[cite_start]The **Internet Control Message Protocol (ICMP)** is the standard for testing these conditions[cite: 395].
* [cite_start]**Normal Conditions:** An "Echo Request" is met with an "Echo Reply"[cite: 396].
* [cite_start]**Failure Conditions:** The source reports a "Request timed out" because the path is broken[cite: 397].

---

## Experiment Methodology

### Task 1: Basic Setup
1. [cite_start]Connect PC0 and PC1 to the 2960 Switch[cite: 407, 408, 410].
2. [cite_start]Assign logical IP addresses to both devices to enable communication[cite: 411].

### Task 2: Establishing a Baseline
* [cite_start]Initiate a ping from **PC0 to PC1**[cite: 413].
* [cite_start]**Observation:** In Simulation Mode, packets move successfully between devices, and "Replies received" is confirmed[cite: 414, 415, 416].

### Task 3: Simulating a Link Failure
1. [cite_start]Start a continuous ping from PC0 to PC1[cite: 418].
2. [cite_start]While the ping is active, disconnect the cable between **PC1 and the Switch**[cite: 420].
3. [cite_start]**Observation:** The simulation displays red indicators showing packet drops, and the CLI reports "Request timed out"[cite: 422, 423, 424].

### Task 4: Network Recovery
1. [cite_start]Reconnect the Copper Straight-Through cable to PC1[cite: 426].
2. [cite_start]Monitor the ping output[cite: 427].
3. [cite_start]**Observation:** After a brief initialization period, ICMP replies resume, indicating that communication has been fully restored[cite: 429, 430].

---

## Conclusion
This experiment highlights the vulnerability of network communication to physical disruptions. [cite_start]It also demonstrates the resilience of standard protocols, showing that once a physical path is restored, logical communication can automatically resume without manual re-configuration[cite: 393, 430].
