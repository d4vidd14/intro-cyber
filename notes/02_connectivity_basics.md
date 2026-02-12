# Connectivity Basics (Key Concepts)

## MAC address
- Usually written as 6 bytes (e.g., AA:BB:CC:DD:EE:FF)
- The first 3 bytes are the OUI (vendor/manufacturer identifier) → useful to identify the device maker.

## IPv4 ranges
- IPv4 addresses go from 0.0.0.0 to 255.255.255.255 (32 bits).

### Special addresses
- 0.0.0.0: "unspecified" / default route context
- 127.0.0.1: loopback (your own machine)
- APIPA: 169.254.0.0/16 → automatic address if DHCP fails (common in Windows)

## Public vs Private IPs
### Public IPs
- Globally routable on the internet.
- Allocation chain: IANA → RIRs → ISPs → organizations/users.

### Private IP ranges (RFC1918)
- 10.0.0.0/8
- 172.16.0.0/12
- 192.168.0.0/16

Common home network concepts:
- Gateway: router IP (e.g., 192.168.1.1)
- Broadcast: last address of the subnet (depends on mask)
- Usable range: all addresses in subnet except network + broadcast

## Subnetting / subnet mask
- Mask splits network vs host part (e.g., /24 == 255.255.255.0)
- Defines:
  - Network address
  - Broadcast address
  - Range of usable host IPs

## DHCP
- Automatically assigns IP, mask, gateway, DNS to clients.
- If DHCP fails, a device may get APIPA (169.254.x.x).

## DNS
- Translates domain names to IP addresses.
- Local override via hosts file (security risk if modified):
  - Can redirect a domain to a malicious IP.

Hosts file locations:
- Windows: C:\Windows\System32\drivers\etc\hosts
- Linux/macOS: /etc/hosts

## Protocols
- TCP: reliable, connection-oriented
- UDP: faster, connectionless
- ICMP: diagnostics (ping), network messages

## Port vs Socket
- Port: logical endpoint number on a host (e.g., 443)
- Socket: (IP, port, protocol) tuple identifying a specific endpoint (and often includes remote side in a connection).
