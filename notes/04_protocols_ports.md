# Protocols, Ports, and Sockets

## Port vs Socket (quick)
- **Port**: logical number on a host used to identify a service (e.g., 443).
- **Socket**: endpoint defined by (IP, port, protocol). In practice, a connection is identified by
  (src IP, src port, dst IP, dst port, protocol).

## Common ports (quick list)
Below are frequent protocols, their typical ports, and notes.

| Protocol | Default Port(s) | Transport | Purpose / Notes | Security notes |
|---|---:|---|---|---|
| FTP | 21 (control), 20 (data) | TCP | File transfer (legacy) | Unencrypted; prefer SFTP/FTPS |
| SFTP | 22 | TCP | File transfer over SSH | Encrypted; uses SSH |
| TFTP | 69 | UDP | Simple file transfer | No auth/encryption; used in PXE/boot |
| SMTP | 25, 587, 465 | TCP | Sending email | 587 submission; TLS recommended |
| POP3 | 110, 995 | TCP | Retrieve email | 995 = POP3S (TLS) |
| IMAP | 143, 993 | TCP | Retrieve/sync email | 993 = IMAPS (TLS) |
| HTTP | 80 | TCP | Web traffic | Unencrypted |
| HTTPS | 443 | TCP | Secure web traffic | TLS; cert validation matters |
| SSH | 22 | TCP | Secure remote shell | Brute-force risk; keys preferred |
| NTP | 123 | UDP | Time synchronization | Time drift impacts auth/logs |
| LDAP | 389, 636 | TCP/UDP | Directory services | 636 = LDAPS (TLS) |
| SNMP | 161 (queries), 162 (traps) | UDP | Network monitoring/management | v1/v2 weak; v3 preferred |
| SIP | 5060, 5061 | UDP/TCP | VoIP signaling | 5061 often TLS |
| RDP | 3389 | TCP/UDP | Remote desktop | High-value target; restrict exposure |

## Port redirection (high level)
A request to one port can be forwarded to another service/port (e.g., via a reverse proxy, NAT rules, or local port forwarding).
This is common in web infrastructure (80→443) or when exposing internal services safely.

## Practical takeaway
- Know what service is expected on a port (baseline).
- Unexpected open ports or insecure protocols (FTP/TFTP/POP3/IMAP without TLS, exposed RDP) are common risks.
