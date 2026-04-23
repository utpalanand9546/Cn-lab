# Lab 10: DNS Server Practical

---

## Objective

To understand and simulate the working of:

* DNS (Domain Name System)
* TCP 3-Way Handshake
* HTTP Communication between client and web server

---

## Network Configuration

The following devices were used in the simulation:

* 1 PC
* 1 Switch
* 1 DNS Server
* 1 Web Server

All devices were connected through the switch.

---

## Procedure / Steps

### Step 1: Open Cisco Packet Tracer

Open Cisco Packet Tracer and place the required network devices in the workspace.

### Step 2: Add and Connect Devices

Add the following devices:

* 1 PC
* 1 Switch
* 1 DNS Server
* 1 Web Server

Connect all devices using appropriate copper straight-through cables.

### Step 3: Configure IP Addresses

Assign IP addresses to:

* PC
* DNS Server
* Web Server

Ensure all devices are in the same network.

### Step 4: Configure DNS Server

Open the DNS Server and go to:

**Services > DNS**

Then:

* Turn the DNS service **ON**
* Add a DNS record:

  * **Name:** `www.kshma.com`
  * **Address:** *(IP address of Web Server)*

### Step 5: Configure the PC

Open the PC and assign:

* IP address
* Subnet mask
* Default gateway (if required)
* **DNS Server IP address**

This allows the PC to resolve the domain name through the DNS server.

### Step 6: Configure the Web Server

Open the Web Server and go to:

**Services > HTTP**

Then:

* Turn the HTTP service **ON**
* Edit the `index.html` file
* Add the required webpage content

### Step 7: Access Website from PC

Open the PC and go to:

**Desktop > Web Browser**

Type the URL:

`http://www.kshma.com`

Then click **Go**.

### Step 8: Run Simulation Mode

Switch to **Simulation Mode** and observe packet movement between the PC, DNS Server, and Web Server.

---

## Packet Movement / Working

The following packet flow was observed during the practical:

### 1. DNS Query Packet

* The PC first sends a **DNS request** to the DNS Server
* This request asks for the IP address of `www.kshma.com`

### 2. DNS Response Packet

* The DNS Server checks its configured DNS records
* It returns the **IP address of the Web Server** to the PC

### 3. TCP Connection Establishment

After resolving the domain name, the PC starts communication with the Web Server using **TCP**.

This happens using the **3-Way Handshake**:

#### a) SYN

* The PC sends a **SYN packet** to the Web Server
* This initiates the TCP connection

#### b) SYN-ACK

* The Web Server replies with a **SYN-ACK packet**
* This acknowledges the request and agrees to establish connection

#### c) ACK

* The PC sends an **ACK packet**
* This completes the TCP connection establishment

### 4. HTTP Request

* After the TCP connection is established, the PC sends an **HTTP request** to the Web Server
* The server receives the request for the webpage

### 5. HTTP Response

* The Web Server sends the contents of the edited `index.html` file back to the PC
* The webpage is successfully displayed in the browser
