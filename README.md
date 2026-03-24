# Cybersecurity Study Journey

This repository documents my learning journey in Cybersecurity.

The goal of this project is to study networking, security fundamentals and cybersecurity tools while documenting everything I learn through practical notes and experiments.

Start date: March 2026

---

## Study Notes (Portuguese)

Detailed study notes written in Portuguese can be found in the **notes** folder.

---

# Day 1 — Network Fundamentals

Today I studied the basic concepts of how networks and the internet work.

## Concepts Learned

### IP (Internet Protocol)

The IP (Internet Protocol) is a unique identifier assigned to each device connected to a network.  
It allows devices to communicate with each other over the internet.

#### Observed IP Address
172.21.5.2

This address belongs to the IPv4 range commonly used in private networks.

---

### IPv4 Address Classes

IPv4 addresses were historically divided into classes that defined the size of the network and the number of possible hosts.

| Class | Range | Typical Use |
|------|------|------|
| A | 1 – 126 | Very large networks |
| B | 128 – 191 | Medium-sized networks |
| C | 192 – 223 | Small networks |

#### How each class is used

**Class A**

- Used for very large networks  
- Few networks but many devices  
- Large host capacity  

**Class B**

- Used for medium networks  
- Balance between number of networks and hosts  
- Example: companies and universities  

**Class C**

- Used for smaller networks  
- Many networks but fewer hosts per network  
- Very common in LAN environments (homes and small offices)

---

### Practical Example

Observed IP: **172.21.5.2**

In a simplified classful view:

Network portion:
172.21

Host portion:
5.2

---

# DNS (Domain Name System)

DNS is a system responsible for translating domain names into IP addresses.

Instead of accessing websites using numeric IP addresses, we use easy-to-remember names and DNS performs the translation automatically.

### How it works

When you type a URL into a browser, for example:

www.google.com

The following happens:

1. The DNS server receives the request
2. The domain name is translated into an IP address
3. The browser uses that IP address to locate and access the correct server

### Summary

DNS converts:

Domain name → IP address

This allows users to access websites easily without memorizing numerical addresses.

Example:

Domain: www.google.com  
IP Address: 142.250.190.78 (example)

---

# HTTP and HTTPS

### HTTP (HyperText Transfer Protocol)

HTTP is a protocol used to transfer data on the web.

It enables communication between:

Client (web browser)  
Server (where the website is hosted)

HTTP sends data in plain text, which means the information could potentially be intercepted.

---

### HTTPS (HyperText Transfer Protocol Secure)

HTTPS is the secure version of HTTP.

The main difference is that it uses encryption to protect the data exchanged between client and server.

Key characteristics:

- The **S** stands for Secure
- Uses encryption protocols such as TLS
- Protects sensitive information like:
  - Passwords
  - Personal data
  - Payment information

### Summary

HTTP → normal communication without encryption

HTTPS → encrypted and secure communication

Today, most websites use HTTPS.

---

# TCP (Transmission Control Protocol)

TCP is a protocol responsible for ensuring that data is transmitted correctly between devices.

It works together with IP as part of the TCP/IP model.

### How TCP works

Before sending data, TCP establishes a connection between the client and the server.

This guarantees:

Connection establishment before data transfer  
Data is sent in organized packets  
Packet delivery confirmation  
Retransmission if data is lost  

### Main Characteristics

Reliable data transmission  
Connection-oriented communication  
Error detection and correction  
Packet ordering and reconstruction  

### Practical Example

When accessing a website using HTTPS, TCP ensures that:

All data arrives completely  
No packets are lost  
The communication remains stable

### Summary

TCP is a reliable transport protocol that ensures data arrives correctly and in the right order.

It is widely used in:

Web browsing (HTTP / HTTPS)  
Email services  
File transfers

---

# Tools Used

- Wireshark (packet analysis)
- Local network traffic observation

---

# Learning Goal

Build a strong foundation in networking and cybersecurity by studying concepts and performing practical analysis.

Future topics will include:

- Network scanning
- Security tools
- Packet analysis
- Vulnerability discovery



## Day 2 — Network Ports

## Network Ports

Ports are numerical identifiers used to distinguish different types of communication within a device connected to a network.

They allow a single computer or server to run multiple services at the same time without mixing the incoming data.

Each port acts as a specific communication channel. When data arrives at a device through the network, the operating system checks the port number and forwards the data to the correct application or service.

For example, a server may simultaneously receive:

- Web page requests
- File transfers
- Email messages

Each of these services uses a different port, ensuring that data is processed correctly.

---

## How Ports Work

When a device communicates over the internet, two key elements are used:

IP Address → Identifies the device on the network  
Port → Identifies which service within the device should receive the data

In practice:

IP + Port = Specific Service

Example:

192.168.1.1:80

192.168.1.1 → Server address  
80 → Port used for the HTTP web service

---

## Port Range

Network ports range from:

0 to 65535

They are divided into three main categories.

### 1. Well-Known Ports (0–1023)

Reserved for standard internet services.

Examples:

| Port | Service |
|-----|------|
| 20/21 | FTP (File Transfer Protocol) |
| 22 | SSH (Secure Shell) |
| 23 | Telnet |
| 25 | SMTP (Email sending) |
| 53 | DNS |
| 80 | HTTP |
| 443 | HTTPS |

---

### 2. Registered Ports (1024–49151)

Used by specific applications and registered services.

Examples:

| Port | Service |
|-----|------|
| 3306 | MySQL |
| 5432 | PostgreSQL |
| 8080 | Alternative HTTP |

---

### 3. Dynamic / Ephemeral Ports (49152–65535)

Temporary ports used by the operating system for outbound connections.

Example:

When your browser accesses a website, it uses a random port from this range.

Example communication flow:

PC:52014 → Server:443

The server responds to the same port, ensuring the data reaches the correct application.

---

## Example of a Web Connection

When accessing a website:

Client computer → random ephemeral port  
Web server → port 80 (HTTP) or 443 (HTTPS)

Example:

PC:52014 → Server:443

This allows the server to send the response back to the correct client process.

---

## Importance of Ports in Network Security

Ports play a critical role in network security.

Security tools analyze which ports are open, closed, or filtered on a system.

Possible states include:

Open → a service is running on the port  
Closed → no service is listening  
Filtered → blocked by a firewall

Attackers often scan systems looking for open ports with vulnerable services.

Port scanning tools help identify these exposures.

---

## Tools Used to Analyze Ports

Common tools used in networking and security include:

- netstat
- ss
- nmap
- lsof

Example command:
nmap 192.168.1.1


This command scans a device to identify which ports are open.

---

## Summary

Ports identify services running inside a device.

They work together with IP addresses to route network communication.

Key points:

- Ports range from 0 to 65535
- They allow multiple services to run simultaneously
- They are essential for networking and cybersecurity
- Open ports can represent potential attack surfaces


## Day 3 — Port Scanning

Today I studied the concept of **port scanning** and how it is used to identify open ports and active services on a system.

### What is Port Scanning

Port scanning is a technique used to discover which ports are open on a device connected to a network.

When a port is open, it usually means that a service is running and listening for incoming connections.

Identifying open ports helps security professionals understand which services are exposed on a system.

---

### Tool Used

For this exercise I used **Nmap**, a widely used network scanning tool.

Nmap allows security analysts and network administrators to scan systems and detect:

- open ports
- closed ports
- filtered ports

It can also help identify the services running on those ports.

---

### Example Command
nmap localhost

This command scans the local machine and checks which ports are open.

---

### Example of Common Ports

| Port | Service |
|-----|------|
| 22 | SSH |
| 53 | DNS |
| 80 | HTTP |
| 443 | HTTPS |

---

### Key Takeaways

- Port scanning is used to discover open ports on a system.
- Open ports usually indicate running services.
- Tools like Nmap help identify exposed services on a network.
- Port scanning is commonly used in cybersecurity, network administration, and penetration testing.