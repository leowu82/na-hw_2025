# HW3 - Mail Server
This project focuses on deploying a fully functional and secure mail server on Debian, integrating DNS, SMTP, IMAP, TLS, and modern anti-spam/authentication mechanisms.

## Key Tasks
- Mail Server Setup
    - Deployed a dedicated VM as `mail.36.nasa` with static IP assignment
    - Configured MX records in DNS with DNSSEC signing to enable email routing
- Core Services
    - Installed and configured Postfix (SMTP) and Dovecot (IMAP/POP3)
    - Enabled STARTTLS/TLS using server-issued certificates for encrypted transmission
    - Integrated SASL authentication between Postfix and Dovecot
- User & Address Management
    - Created system accounts (`ta`, `cool-ta`) with secure authentication
    - Implemented aliases, sub-addressing (`+tag`), and sender rewriting for flexible mail delivery
- Security Features
    - Restricted sender addresses to prevent spoofing
    - Blocked null senders and disabled open relay functionality
    - Configured DNS-based protections:
        - SPF – restrict domain to authorized mail server IP
        - DKIM – signed outgoing mail with domain key, verified inbound mail
        - DMARC – enforced reject policy for failed SPF/DKIM checks
    - Integrated greylisting (postgrey) and header-based spam filters
- Debugging & Verification
    - Tested TLS handshakes with `openssl s_client`
    - Verified DNS and mail records with `dig` and log inspection (`journalctl`)

## Skills Demonstrated
- DNS + MX record management with DNSSEC
- Postfix and Dovecot administration (SMTP, IMAP, TLS)
- Mail authentication standards: SPF, DKIM, DMARC
- Anti-spam measures: greylisting, regex-based header filtering
- Secure mail relay and sender policy enforcement
- Systemd service management and debugging

## Notes:
https://sun-ski-6a4.notion.site/HW3-Mail-Server-1d9768cf5f3580ae81ddfa1758560b85?source=copy_link
