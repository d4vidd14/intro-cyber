# Connectivity Commands (Windows)

## Show IP configuration
ipconfig
ipconfig /all

Look for:
- IPv4 Address
- Subnet Mask
- Default Gateway
- DNS Servers
- Physical Address (MAC)

## Check hosts file (read-only)
Path: C:\Windows\System32\drivers\etc\hosts

Security note:
- If a malicious entry is added, it can redirect a domain to a wrong IP.
