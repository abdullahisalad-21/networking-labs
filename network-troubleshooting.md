# Network Troubleshooting

## Overview
Troubleshooting is a core IT skill. These steps help identify and fix network issues quickly.

---

## 1. Check Physical Layer
- Is the cable plugged in  
- Are switch lights active  
- Is Wi-Fi enabled  

---

## 2. Check IP Configuration
ipconfig /all

---

## 3. Test Connectivity
ping 8.8.8.8

---

## 4. Test DNS
nslookup google.com

---

## 5. Trace Route
tracert google.com

---

## 6. Common Issues
- Wrong IP address  
- Wrong gateway  
- DNS server offline  
- DHCP not assigning IP  
- Firewall blocking traffic  

---

## What I Learned
- How to diagnose connectivity issues  
- How to isolate DNS vs routing problems  
- How to follow a structured troubleshooting process  



## Scenario: DNS not working

A user could browse using IP addresses but not website names.  
I tested DNS:

nslookup google.com

It failed.  
I flushed DNS:

ipconfig /flushdns

Then tested again — DNS resolved correctly.
