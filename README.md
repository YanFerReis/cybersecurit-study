## Study Notes (Portuguese)

Detailed study notes can be found in the notes folder.

# Cybersecurity Study Journey

This repository documents my learning journey in Cybersecurity.

The goal of this project is to study networking, security fundamentals and cybersecurity tools while documenting everything I learn through practical notes and experiments.

Start date: March 2026

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
