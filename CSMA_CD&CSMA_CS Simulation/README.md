# Lab 6 : CSMA/CD and CSMA/CA Simulation

---

## Objective

To understand and simulate the working of:

* CSMA/CD (Collision Detection)
* CSMA/CA (Collision Avoidance)

---

## Procedure / Steps

### CSMA/CD Simulation

1. Open Cisco Packet Tracer

2. Add 4 PCs connected via a Hub

3. Configure IP addresses for all PCs

4. Data Transmission Setup

   * Select 2 PCs as sender devices
   * Send data packets to the other PCs
   * Set:

     * Sequence Number = 1
     * Periodic Interval = 1

5. Run Simulation Mode

   * Switch to Simulation Panel
   * Start packet transmission

6. Observation

   * Observe packet collisions when multiple devices transmit simultaneously
   * Monitor retransmission after collision detection

---

### CSMA/CA Simulation

1. Open Cisco Packet Tracer

2. Add 4 Laptops

   * Install WPC300 wireless module in each laptop

3. Add an Access Point (ACCESS POINT-PT-AC)

4. Configure Wireless Connection

   * Connect all laptops to the access point via Wi-Fi

5. Data Transmission Setup

   * Select 2 laptops as sender devices
   * Send data packets to the remaining laptops
   * Set:

     * Sequence Number = 1
     * Periodic Interval = 1

6. Run Simulation Mode

   * Switch to Simulation Panel
   * Start packet transmission

7. Observation

   * Observe how collisions are avoided during transmission
   * Monitor controlled data flow between devices
