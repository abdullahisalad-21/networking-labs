**📝 Networking Lab — Remote Connections, SSH, and Infrastructure Behavior
📘 Overview**
Today I worked on remote connections, SSH configuration, and understanding how different infrastructure environments (WSL vs VirtualBox) behave when running network services. 
I practiced real-world system administration by connecting my VirtualBox Ubuntu VM and my WSL Ubuntu environment using SSH in both directions. 
I also tested GUI application behavior over SSH and summarized Module 2’s remote access reading.
**🎯 Objectives**
• 	Install and verify SSH on both WSL and VirtualBox
• 	Compare network interfaces and IP addressing
• 	Establish SSH connections between systems
• 	Understand why GUI apps fail over SSH
• 	Summarize remote access tools (SSH, RDP, VPN, RMM)
• 	Strengthen my Module 2 networking knowledge
**🛠️ Tools & Commands Used**
- sudo apt install openssh-server openssh-client
- sudo service ssh status
- ip a
- ssh user@IP
- ls -l
- whereis
- sudo apt install ./discord.deb
- Concepts: SSH, X11, WSLg, NAT, Host‑Only networking
**🚀 Steps Completed**
1. Installed SSH on WSL
I installed the SSH server and client. WSL generated RSA, ECDSA, and ED25519 host keys and created socket activation links.
2. Verified SSH service behavior
- On VirtualBox Ubuntu, SSH was active and running normally.
- On WSL Ubuntu, SSH was initially inactive.
- After manually starting it, SSH became active and listening on port 22.
- 3. Compared network interfaces
VirtualBox Ubuntu:
- NAT: 10.0.2.15
- Host‑Only: 192.168.56.103 (reachable from Windows/WSL)
WSL Ubuntu:
- eth0: 172.29.97.52
4. Connected systems using SSH
- From WSL → VirtualBox: ssh iskutashi@192.168.56.103
- From VirtualBox → WSL: ssh iskutashi@172.29.97.52
This created a real multi‑machine remote administration environment
5. Tested GUI application (Discord)
I installed Discord using a .deb file, but it failed to launch because:
- SSH sessions have no display server
- $DISPLAY was not set
- WSL GUI apps cannot run over remote SSH
6. Summarized remote access reading
I reviewed SSH, RMM, RDP, VPN, cloud file sharing, remote work trends, and security risks.
**🐞 Problems & Fixes**
- SSH inactive on WSL → I started it manually with sudo service ssh start.
- GUI app failed over SSH → I learned GUI apps require a display server and cannot run in a terminal-only SSH session.
- IP confusion → I identified correct IPs and understood NAT vs Host‑Only vs WSL networking.
**🧠 What I Learned**
- SSH behaves differently depending on the infrastructure layer.
- VirtualBox acts like a real server; WSL behaves like a developer environment.
- GUI apps cannot run over SSH without X11/Wayland.
- Host‑Only networking is ideal for VM-to-host communication.
- Remote access tools each serve different use cases.
- Multi‑machine labs are essential for mastering system administration.
**📎 Related Files**
- discord.deb
- SSH host keys
- Network interface outputs.
**➡️ Next Steps**
- Configure SSH key-based authentication
- Practice SFTP/SCP file transfers
- Begin DNS and DHCP labs
- Explore systemd service management
- Document remote access security best practices

