# Network-Pivoting-Proxychains-sshuttle-Lab
This repository showcases network pivoting techniques using Proxychains and sshuttle, including internal network reconnaissance, TCP-based Nmap scanning, and tool comparison in a post-exploitation scenario.

# Network Pivoting Using Proxychains and sshuttle

## Overview
This project demonstrates **network pivoting and lateral movement** by leveraging a compromised host to access an otherwise unreachable internal network. Proxy-based tunneling and transparent routing techniques were evaluated using **Proxychains** and **sshuttle**.

## Environment
- Attacker Machine: Linux
- Compromised Host: 10.10.155.5/24
- Target Internal Network: 10.10.10.0/24
- Tools: Proxychains, sshuttle, Nmap, SSH

## Initial Reconnaissance
- Identified network interfaces and IP addresses on the compromised host
- Confirmed lack of direct routing to the internal network via ICMP

## Pivoting with Proxychains
- Configured SOCKS proxy in `/etc/proxychains4.conf`
- Utilized Proxychains to route traffic through the compromised host
- Conducted TCP-based Nmap scans (`-sT`) against internal network assets
- Demonstrated proxy-based access for post-exploitation activities

## Pivoting with sshuttle
- Established a transparent VPN-like tunnel to the internal network
- Enabled direct access to internal hosts without application-level proxying
- Compared ease of use and performance against Proxychains

## Comparison & Reflection
- Proxychains requires per-tool proxy configuration but offers granular control
- sshuttle provides seamless network access with minimal configuration
- Both tools are effective depending on engagement requirements

## Disclaimer
All activities were performed in a controlled lab environment for **educational purposes only**.
