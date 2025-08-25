# HW2 - DNS
This project explores the setup and administration of Domain Name System (DNS) services using BIND9 on Debian, including custom zone files, reverse DNS, resolvers, and DNS security extensions (DNSSEC).

## Key Tasks
- DNS Server Setup
    - Installed and configured BIND9
    - Created custom forward and reverse zones (`36.nasa` and `36.168.192.in-addr.arpa`)
    - Verified syntax and functionality with `named-checkconf`, `named-checkzone`, and `dig`
- Zone Files
    - Defined authoritative records for hosts (`A`, `NS`, `PTR`)
    - Configured reverse lookup zones for IP-to-domain resolution
- Resolver Configuration
    - Enabled recursion with global and zone-specific forwarders
    - Integrated public DNS forwarders (e.g., Cloudflare `1.1.1.1`)
- DNSSEC
    - Generated ZSK/KSK key pairs using `dnssec-keygen`
    - Signed forward and reverse zones with `dnssec-signzone`
    - Configured chain of trust and verified with `dig +dnssec`
- Security & Extensions
    - Explored DNS over TLS (DoT) and DNS over HTTPS (DoH) support in BIND9
    - Managed permissions and service restarts for secure operation

## Skills Demonstrated
- BIND9 DNS server administration
- Forward/reverse zone configuration
- DNSSEC signing and validation (ZSK/KSK, DS records, chain of trust)
- Resolver setup with recursion and forwarders
- Debugging with dig and journalctl
- Understanding of secure DNS protocols (DoT/DoH)

## Notes:
https://sun-ski-6a4.notion.site/HW2-DNS-1be768cf5f358052aca1c97a2c239e78?source=copy_link
