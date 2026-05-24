# Cybersecurity Home Lab Documentation

## Lab Setup

This home lab was created to practice cybersecurity concepts including network scanning, traffic analysis, and basic system security.

## Virtual Machines

- Kali Linux (Attacker Machine)
- Lubuntu (Target Machine)

## System Configuration

- RAM: 2GB
- CPU: 2 cores
- Network: Host-only + NAT

## Tasks Performed

### Networking
- IP addressing
- MAC addressing
- ARP
- Routing
- DNS
- Gateway
- Subnetting

### Scanning
- Used Nmap to scan open ports
- Identified SSH (port 22) and HTTP (port 80)

### Remote Access
- Connected to Lubuntu using SSH

### Packet Analysis
- Captured traffic using Wireshark
- Analyzed ICMP (ping)
- Compared HTTP vs SSH traffic

### Web Testing
- Created a simple login page
- Observed credentials in HTTP packets

## SSH and user Management
Activities
- installed OpenSSH Server
- Connected Remotely Using SSH
- Created Linux users
- Observed file permissions

Key Learning
SSH enables secure remote administration and linux permissions control user access

## Linux Logs and Monitoring

### Activities
- Observed authentication logs
- Detected failed logins
- Viewed active users
- Identified listening services

## Linux Hardnening

Activities:
- Updated Packages
- User management
- Permission changes
- SSH hardnenig
- Firewall setup

Learning:
Hardening reduces attack surface and improve security

## Screenshots

### Nmap Scan

![Nmap](screenshots/nmap-scan.png)

### SSH Login

![SSH](screenshots/ssh-login.png)

### Firewall Rules

![Firewall](screenshots/firewall-rules.png)

### Wireshark Capture

![Wireshark](screenshots/wireshark-capture.png)
logs help analysts investigate authentication and systen behavior

