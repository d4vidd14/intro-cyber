# Blue Team Concepts (Defensive Security)

## Visibility & control
- **Shadow IT**: tools/services used without approval (risk: unknown data flows, weak controls).
- **Endpoint**: user devices (laptops, desktops, mobiles) where attacks often start.
- **Proxy**: intermediary for traffic; can filter, log, and enforce policy.

## Secure connectivity
- **VPN**: encrypted tunnel for remote access or site-to-site connectivity.

## Detection concepts
- **IOC (Indicator of Compromise)**: evidence suggesting compromise (hashes, domains, IPs, filenames, registry keys, etc.).
- **Honeypot**: decoy system to detect and study attacker behavior.
- **IDS/IPS**: detection / prevention systems for suspicious traffic.

## Malware protection
- **EPP / AV (Endpoint Protection Platform / Antivirus)**: baseline prevention and signature/behavior detection.
- **EDR (Endpoint Detection & Response)**: deeper telemetry + detection + investigation + response actions on endpoints.
- **MDR (Managed Detection & Response)**: outsourced monitoring/response service (often built on EDR/SIEM).

## Data protection
- **Encryption / Cryptography**: protects confidentiality (e.g., TLS, disk encryption).
- **Hashing**: integrity checks and identification (e.g., file hashes for IOCs).
- **DLP (Data Loss Prevention)**: prevents sensitive data from leaving the organization (email, web, endpoints).

## Monitoring & operations
- **SIEM**: collects/correlates logs and alerts (central visibility).
- **SOC (Security Operations Center)**: people + process + tools that monitor, triage, investigate and respond.
- **Threat hunting**: proactive search for suspicious activity (not just reacting to alerts).

## Security in development
- **DevSecOps**: integrating security into CI/CD and development lifecycle (shift-left + automation).
- **AppSec**: application security practices (secure coding, testing, dependency scanning, etc.).
- **WAF (Web Application Firewall)**: protects web apps against common attacks (often at L7).

## Access control
- **ACL (Access Control List)**: rules defining allowed/denied access (network/filesystems).
- **MFA/2FA**: multi-factor authentication (reduces account takeover risk).
- **IAM / GDI (Identity & Access Management / directory services)**: managing identities, roles, permissions (e.g., AD/Entra).

## Hardening
- **Hardening**: reducing attack surface by secure configuration (patching, least privilege, disabling unnecessary services).

## Practical takeaway
- Blue Team is about: visibility → detection → response → continuous improvement.
- Many controls are strongest when combined: IAM/MFA + hardening + endpoint visibility + SIEM/SOC processes.
