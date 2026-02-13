# Red Team / Blue Team Concepts (Terminology)

## Roles & ethics
- **White hat**: authorized, ethical security testing.
- **Gray hat**: may act without full authorization or in legal/ethical gray areas.
- **Black hat**: malicious hacking for personal gain/damage.

## Common terms
- **Script**: automated set of commands/instructions to perform a task.
- **Exploit**: code/technique that takes advantage of a vulnerability.
- **Metasploit**: framework for developing/executing exploits and payloads (used for testing).
- **Bug**: flaw/defect in software; may become a vulnerability.
- **PoC (Proof of Concept)**: minimal demonstration that a vulnerability is real.
- **APT (Advanced Persistent Threat)**: long-term, stealthy adversary operations (often well-resourced).
- **APT “cheat sheet”**: mapping of tactics/techniques (often aligned with MITRE ATT&CK).

## Botnet concepts
- **Bot/Zombie**: compromised machine controlled remotely.
- **Botnet**: network of bots controlled by an attacker.

## Recon / Information gathering
- **Gathering / Recon**: collecting information about target systems (domains, IP ranges, tech stack, employees).
- **Metadata**: hidden/embedded info in files (author, software, timestamps, geolocation) that can leak details.
- **Tracing**: tracking origin/route/ownership of infrastructure (domains, IPs, hosting, email headers).

## Attack concepts (high level)
- **Privilege escalation**: gaining higher permissions (e.g., user → admin/root).
- **Backdoor**: hidden access mechanism to regain entry.
- **Enumeration**: deeper discovery after initial access (users, shares, services, versions).
- **Post-exploitation**: actions after access to understand impact (credentials, persistence, lateral movement).
- **Pivoting / Tunneling**: using a compromised system to access/internal networks that are otherwise unreachable.
- **Hijacking**: taking control of a session/connection/resource (term varies by context).
- **Buffer overflow**: memory corruption caused by writing beyond buffer boundaries (can lead to code execution).

## “Jail” / isolation concepts
- **chroot (jail)**: restricts a process to a directory subtree (not full security isolation by itself).
- **Linux capabilities**: fine-grained privileges for processes (instead of full root).
- **CTF Jailbreak**: challenge type where you escape a restricted environment (educational context).

## Network/Service discovery
- **Banner grabbing**: reading service banners to identify software/version (useful for inventory & risk assessment).

## Social engineering / fraud terms (awareness)
- **Scam**: deception to obtain money/data.
- **Hoax**: false information meant to mislead.
- **Phreaking**: attacks related to telephony systems (historical/modern variants).
- **Carding**: credit card fraud-related activity.
- **Trashing**: searching discarded material for sensitive info.
- **Boxing**: term sometimes used for “cable box”/TV piracy contexts (varies; best treated as illegal/fraud context).

## Pentesting vs Red Team (methodology)
- **Penetration testing**: scoped, time-boxed security assessment to find and validate vulnerabilities.
- **Red Team**: adversary emulation focused on achieving objectives and testing detection/response, usually stealthier and more realistic.
- Typical phases:
  1) Recon/Gathering
  2) Scanning & enumeration
  3) Exploitation (authorized)
  4) Post-exploitation (impact, evidence)
  5) Reporting (findings, risk, remediation)

## Practical takeaway
- Focus on legality/authorization and on translating findings into clear risk and remediation.
- Defensive value: these concepts help understand attacker behavior and improve detection and controls.
