# Lab 3: TCP Simulation

---

## Objective

To understand and simulate the working of:

* TCP (Transmission Control Protocol)

---

## Procedure / Steps

### TCP Simulation

1. Open Cisco Packet Tracer

2. Add the following devices:

   * 1 PC
   * 1 Switch
   * 1 Server

3. Connect the devices:

   * Connect the **PC to the Switch**
   * Connect the **Server to the Switch**

4. Configure IP addresses:

   * Assign an IP address to the **PC**
   * Assign an IP address to the **Server**
   * Ensure both devices are in the same network

5. Configure the Server:

   * Open the **Server**
   * Go to **Services**
   * Enable the **HTTP service**

6. Access the Server from PC:

   * Open the **PC**
   * Go to **Desktop > Web Browser**
   * Enter the **IP address of the Server**
   * Click **Go**

7. Run Simulation Mode:

   * Switch to **Simulation Panel**
   * Start the simulation
   * Observe the communication between PC and Server

---

## Packet Movement

During the simulation, the following packet movement can be observed:

1. **PC sends TCP connection request (SYN)**

   * The PC initiates communication with the Server

2. **Server replies with SYN-ACK**

   * The Server acknowledges the request and responds

3. **PC sends ACK**

   * The PC confirms the connection establishment

4. **HTTP Request is sent**

   * The PC requests the webpage from the Server

5. **Server sends HTTP Response**

   * The Server sends the requested webpage/data to the PC

6. **TCP ensures reliable delivery**

   * Packets are delivered in order without loss


