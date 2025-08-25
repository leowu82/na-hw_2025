# HW4 - LDAP
This project implements a secure LDAP (Lightweight Directory Access Protocol) infrastructure to provide centralized authentication, authorization, and directory services across multiple machines.

## Key Tasks
- Server Deployment
    - Configured a dedicated VM running OpenLDAP (slapd) with TLS/SSL encryption (LDAPS only)
    - Integrated with DNS (A record + DNSSEC signed zone)
- Client Integration
    - Connected a workstation VM to authenticate users via LDAP using `libnss-ldap`, `libpam-ldap`, and `nscd`
    - Configured PAM for:
        - Password-based authentication via LDAP
        - Automatic home directory creation on first login (`pam_mkhomedir`)
    - Enabled SSH key-based logins by fetching `sshPublicKey` attributes directly from LDAP
- Directory Information Tree (DIT)
    - Designed and populated a hierarchical structure:
        - `dc=36,dc=nasa` (domain root)
        - Organizational units: `People`, `Group`, `MemberGroup`, `Ppolicy`, `SUDOers`
        - POSIX groups: `ta`, `stu`
        - Users: `generalta`, `stu36` with hashed passwords and SSH keys
- Advanced Features
    - Sudo Integration: Extended schema to include `sudoRole` entries, allowing fine-grained sudo permissions via LDAP
    - Access Control Lists (ACLs): Defined per-attribute and per-user access rules (e.g., password self-write, SSH key management)
    - Custom Schema (Fortunes): Added a new schema to store “fortune” entries with author and ID attributes; imported data from YAML → LDIF conversion
    - SSSVLV Overlay: Enabled server-side sorting and virtual list view for efficient querying and paging

## Security Enhancements
- Enforced TLS-only (LDAPS) communication with server-issued certificates
- Restricted attribute-level access via ACLs (least privilege)
- Required password hashing with SSHA for user entries
- Configured group-based SSH access (`AllowGroups`)

## Skills Demonstrated
- OpenLDAP administration and schema design
- Secure authentication integration with Linux PAM and NSS
- Centralized SSH key management through LDAP attributes
- ACL configuration for fine-grained access control
- Extending LDAP with custom schemas and overlays
- Automating user, group, and sudo role provisioning via LDIF

## Notes:
https://sun-ski-6a4.notion.site/HW4-LDAP-1ed768cf5f358032aadfdd5f304af0d0?source=copy_link
