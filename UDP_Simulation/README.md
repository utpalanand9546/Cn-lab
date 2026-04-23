# Lab 4: UDP Simulation

---

## Objective

To understand and simulate the working of:

* UDP (User Datagram Protocol)

---

## Procedure / Steps

### UDP Simulation

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

5. Configure DNS Service on Server:

   * Open the **Server**
   * Go to **Services > DNS**
   * Turn **DNS Service ON**
   * Add a DNS entry:

     * **Name:** (your domain name, e.g., example.com)
     * **Address:** (Server IP address)

6. Access Server using DNS Name:

   * Open the **PC**
   * Go to **Desktop > Command Prompt or Web Browser**
   * Enter the **DNS name** instead of IP address
   * Send the request

7. Run Simulation Mode:

   * Switch to **Simulation Panel**
   * Start the simulation
   * Observe communication

---

## Packet Movement

During the simulation, the following packet flow can be observed:

1. **PC sends DNS Query (UDP)**

   * The PC requests the IP address corresponding to the domain name

2. **Server processes DNS request**

   * The server checks its DNS table

3. **Server sends DNS Response (UDP)**

   * The server returns the mapped IP address

4. **PC receives IP address**

   * The domain name is resolved successfully

5. **Further communication (if any)**

   * The PC can now communicate using the resolved IP

---
