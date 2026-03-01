📘 Overview
Today I performed a DNS resolution lab across Windows, Ubuntu VM, and WSL. I tested DNS queries, installed missing DNS tools, and validated internal DNS behavior.
🎯 Objectives
- Perform DNS lookups on multiple systems
- Compare Windows vs Linux DNS behavior
- Install DNS utilities on Ubuntu
- Validate internal DNS server responses
- Confirm IPv4 and IPv6 resolution
🛠️ Tools & Commands Used
- nslookup
- dig
- host
- ping
- ipconfig /all
- sudo apt install dnsutils
🚀 Steps Completed
- Ran nslookup facebook.com on Windows and captured DNS server 10.221.121.78.
- Verified IPv4 and IPv6 addresses returned by the resolver.
- Used ping to confirm connectivity and TTL values.
- Attempted DNS queries on WSL and installed dnsutils to enable tools.
- Ran nslookup and dig on Ubuntu to compare results.
- Confirmed that internal DNS servers resolve public domains correctly.
- Compared DNS behavior between Windows, Ubuntu VM, and WSL.
🐞 Problems & Fixes
- Problem: DNS tools missing on WSL.
Fix: Installed dnsutils.
- Problem: Needed to verify internal DNS behavior.
Fix: Used multiple tools (nslookup, dig, ping) to confirm.
🧠 What I Learned
- How internal DNS servers respond to public domain queries
- Differences between Windows and Linux DNS tools
- How to use dig for deeper DNS inspection
📎 Related Files
- DNS query outputs
- WSL DNS tool installation logs
