# Basic Networking Commands

## Overview
These commands are the foundation of network troubleshooting. They help diagnose connectivity, DNS issues, routing problems, and general network health.

---

## 1. ipconfig

### View full network configuration
ipconfig /all

Shows:
- IP address  
- Subnet mask  
- Default gateway  
- DNS servers  
- MAC address  
- DHCP information  

### Why it matters
Understanding IP configuration is the first step in diagnosing any network issue.

---

## 2. ping

### Test connectivity
ping 8.8.8.8 ping google.com

Used to:
- Check if a host is reachable  
- Measure latency  
- Test DNS resolution  

---

## 3. tracert

### Trace the route packets take
tracert google.com

Shows:
- Each hop  
- Latency per hop  
- Where packets fail  

---

## 4. nslookup

### Test DNS resolution
nslookup microsoft.com

Used to:
- Check DNS server response  
- Diagnose DNS failures  

---

## 5. arp

### View ARP table
arp -a

Shows:
- IP-to-MAC mappings  
- Local network device discovery  

---

## What I Learned
- How to test connectivity  
- How DNS works  
- How routing paths are traced  
- How to diagnose local network issues  
