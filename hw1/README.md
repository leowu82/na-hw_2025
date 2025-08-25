# HW1 - Network Config
This project documents the setup and configuration of a Debian-based virtual machine. The goal was to configure core networking services, security policies, and routing to simulate a functional router/server environment.

## Key Tasks
- System Setup
	- Installed Debian on a VM with custom network interfaces
	- Configured `sudo` privileges and enabled SSH remote access
- VPN & Networking
	- Installed and configured WireGuard with auto-boot
	- Set up static IPs and DNS via `/etc/network/interfaces`
	- Enabled IPv4 forwarding for packet routing
- Services
	- Installed and configured a DHCP server to manage dynamic IP assignment
- Firewall & Security
  	- Configured iptables rules for NAT, forwarding, and access control
  	- Implemented custom firewall policies:
    	- Dropped SSH access from VPN to router
    	- Allowed controlled SSH/HTTP/HTTPS traffic
    	- Blocked inbound connections from Internet/VPN to private LAN
  	- Persisted rules with `netfilter-persistent`

## Skills Demonstrated
- Linux system administration (Debian 12)
- VPN setup with WireGuard
- Network routing, NAT, and firewall management using iptables
- DHCP configuration for LAN environments
- Practical understanding of server/network security

## Notes: 
https://sun-ski-6a4.notion.site/HW1-Network-Config-1ab768cf5f3580ad96d7efdc04dce47d?source=copy_link
