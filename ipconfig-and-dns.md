# IPConfig and DNS Troubleshooting

## Overview
DNS issues are one of the most common problems in IT support. These commands help diagnose and fix them.

---

## 1. View DNS Configuration
ipconfig /all

Look for:
- DNS servers  
- DHCP vs static  
- Connection-specific DNS suffix  

---

## 2. Flush DNS Cache
ipconfig /flushdns

Fixes:
- Wrong DNS entries  
- Cached outdated IPs  

---

## 3. Renew IP Address
ipconfig /release ipconfig /renew

Used when:
- DHCP fails  
- IP conflicts occur  
- Network changes happen  

---

## 4. Test DNS Resolution
nslookup google.com nslookup 8.8.8.8

---

## What I Learned
- How DNS resolution works  
- How to fix DNS cache issues  
- How DHCP assigns IP addresses  
- How to diagnose DNS failures  
