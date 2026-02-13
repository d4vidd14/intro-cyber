# Common Attacks (High-Level Overview)

> This note is for defensive understanding: what the attack is, why it matters, and typical mitigations.

## Credential & access attacks
### Brute force
- **What**: repeated login attempts to guess passwords.
- **Signals**: many failed logins from same IP/user, unusual geolocation, bursts in auth logs.
- **Mitigations**: MFA, rate limiting, account lockout, strong passwords, monitoring.

### Phishing
- **What**: tricking users into revealing credentials or running malicious actions.
- **Signals**: suspicious emails/URLs, unusual login patterns, new forwarding rules, user reports.
- **Mitigations**: user awareness, email filtering, MFA, URL protection, reporting workflow.

### Keyloggers
- **What**: malware that captures keystrokes (often to steal credentials).
- **Signals**: suspicious processes, AV/EDR alerts, abnormal outbound connections.
- **Mitigations**: EDR/AV, least privilege, patching, application control.

## Availability attacks
### DoS / DDoS
- **What**: overwhelming a service with traffic/requests to make it unavailable.
- **Signals**: traffic spikes, high CPU/memory, saturated bandwidth, 5xx errors.
- **Mitigations**: rate limiting, WAF/CDN, DDoS protection services, autoscaling, runbooks.

## Exploitation concepts
### Exploiting
- **What**: abusing a vulnerability to execute actions (read/modify data, code execution).
- **Mitigations**: patching, secure configuration, segmentation, vulnerability management.

### Zero-day
- **What**: vulnerability unknown to vendor/public, no patch initially.
- **Mitigations**: defense-in-depth, EDR, monitoring, segmentation, rapid response capability.

## Network deception/manipulation
### Spoofing
- **What**: forging identity (IP/MAC/email/domain) to appear trusted.
- **Mitigations**: authentication, SPF/DKIM/DMARC for email, network controls, monitoring.

### MITM (Man-in-the-Middle)
- **What**: attacker intercepts/changes traffic between two parties.
- **Signals**: certificate warnings, unusual ARP entries, DNS anomalies.
- **Mitigations**: TLS/HTTPS, certificate validation, secure Wi-Fi, VPN.

### Pharming
- **What**: redirecting users to malicious sites by tampering with DNS/hosts/router settings.
- **Mitigations**: secure DNS, protect DNS/routers, monitor DNS changes, endpoint protections.

### Sniffing
- **What**: capturing network traffic (especially dangerous if unencrypted).
- **Mitigations**: encryption (TLS), secure Wi-Fi, segmentation, limit plaintext protocols.

## Recon & tooling
### Scanners
- **What**: tools to discover hosts/services/vulnerabilities.
- **Defensive use**: asset inventory, exposure checks, vulnerability scanning.
- **Mitigations**: minimize exposure, firewall rules, detection of scanning patterns.

## Data integrity attacks
### Data corruption
- **What**: unauthorized modification or destruction of data.
- **Mitigations**: backups, access control, integrity monitoring, change management.

## Web application attacks
### SQL Injection (SQLi)
- **What**: injecting SQL via untrusted input to read/modify DB data.
- **Mitigations**: parameterized queries, input validation, least privilege, WAF (as extra).

### XSS (Cross-Site Scripting)
- **What**: injecting scripts into web pages that run in users’ browsers.
- **Mitigations**: output encoding, CSP, input validation, secure frameworks.

## Human factor
### Social engineering
- **What**: manipulating people to bypass controls (phone, email, impersonation).
- **Mitigations**: training, verification processes, least privilege, MFA, reporting culture.
