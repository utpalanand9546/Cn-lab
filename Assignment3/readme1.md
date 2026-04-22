# Effect of Network Load on Delay and Packet Drops

## Project Overview
[cite_start]This project explores the impact of **network load** on performance within a Local Area Network (LAN)[cite: 241]. [cite_start]By utilizing **Cisco Packet Tracer’s Simulation Mode**, we observe how simultaneous data transmissions lead to network congestion, resulting in increased latency and potential packet loss[cite: 243, 255].

---

## Experiment Objectives
* [cite_start]Generate simultaneous traffic in a LAN environment to observe behavior under higher load[cite: 243].
* [cite_start]Interpret simulation behavior including increased delays and packet drops[cite: 243, 244].
* [cite_start]Analyze network behavior step-by-step using Simulation Mode[cite: 269].

## Hardware & Software Requirements
* [cite_start]**Software:** Cisco Packet Tracer[cite: 246].
* [cite_start]**Switch:** 1x Cisco 2960[cite: 247].
* [cite_start]**End Devices:** 6x PCs (PC0 through PC5)[cite: 248].
* [cite_start]**Connections:** Copper Straight-Through cables[cite: 249].

---

## Core Networking Concepts

### Network Load and Congestion
[cite_start]When multiple devices send data simultaneously, the network experiences **load** or traffic[cite: 250]. [cite_start]As load increases, switches must handle more packets, leading to **network congestion**[cite: 251, 255]. This results in:
* [cite_start]**Delay (Latency):** Packets take longer to reach their destination[cite: 252].
* [cite_start]**Queueing:** Packets must wait in a buffer for processing[cite: 253].
* [cite_start]**Packet Drops:** Packets are discarded when the switch buffer is full[cite: 254].

### ICMP Traffic
[cite_start]The **Internet Control Message Protocol (ICMP)**, used by the `ping` command, is utilized to test connectivity and measure delay[cite: 256, 257].
* [cite_start]**Low Traffic:** Characterized by fast replies[cite: 258].
* [cite_start]**High Traffic:** Results in delayed or lost replies[cite: 259].

---

## Methodology

### Task 1: Baseline Test (Low Traffic)
1. [cite_start]Set up 6 PCs connected to a single 2960 switch using Copper Straight-Through cables[cite: 274, 275, 276, 277].
2. [cite_start]Assign IP addresses to all PCs[cite: 278].
3. [cite_start]Trigger a single ping from **PC0 to PC5** in Simulation Mode[cite: 279, 280].
4. [cite_start]**Observation:** Smooth packet flow with no delay and no packet drops[cite: 282, 283, 284].

### Task 2: High Traffic Test
1. [cite_start]Start three simultaneous pings to create load[cite: 286]:
    * [cite_start]PC0 → PC5 [cite: 287]
    * [cite_start]PC1 → PC4 [cite: 288]
    * [cite_start]PC2 → PC3 [cite: 289]
2. [cite_start]**Observation:** Packets overlap in the simulation, delay increases, and the event list becomes crowded[cite: 291, 292, 294]. [cite_start]Packet queueing is observed, and some packets may be dropped[cite: 293, 302].

---

## [cite_start]Observation Summary [cite: 295]

| Metric | [cite_start]Low Traffic (Baseline) [cite: 296] | [cite_start]High Traffic (Load) [cite: 300] |
| :--- | :--- | :--- |
| **Communication** | [cite_start]Smooth communication [cite: 297] | [cite_start]Increased delay [cite: 301] |
| **Switch Behavior** | [cite_start]No delay [cite: 283] | [cite_start]Packet queueing observed [cite: 302] |
| **Packet Loss** | [cite_start]No packet loss [cite: 298] | [cite_start]Some packet drops possible [cite: 303] |
| **Response Time** | [cite_start]Fast response time [cite: 299] | [cite_start]Slower response time [cite: 304] |

## Conclusion
[cite_start]The experiment demonstrates that shared bandwidth and switch buffer limitations in a LAN can lead to congestion[cite: 260, 262, 263]. [cite_start]Increasing network load directly correlates with higher latency and the risk of packet loss as switch queues fill up[cite: 263, 264].
