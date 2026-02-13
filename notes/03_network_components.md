# Network Components (Overview)

## Firewalls
- **Firewall (stateful)**: filters traffic based on rules (IP/port/protocol), often tracks connection state.
- **UTM (Unified Threat Management)**: firewall + multiple security features in one box (e.g., AV, web filtering, VPN).
- **NGFW (Next-Gen Firewall)**: adds application awareness, IDS/IPS capabilities, user identity, threat intelligence, deeper inspection.

## Network Devices
- **Bridge**: connects two network segments at L2, forwards frames based on MAC addresses.
- **Hub**: L1 repeater; broadcasts everything to all ports (legacy, insecure, collisions).
- **Switch**: L2 device; forwards based on MAC table; reduces collisions; can use VLANs.
- **Multilayer switch**: L2 + L3 capabilities (can route between VLANs).

- **Router**: L3 device; routes traffic between networks/subnets; often performs NAT.
- **Access Point (AP)**: provides Wi-Fi; bridges wireless clients to wired network.
- **Wireless Controller**: centrally manages multiple APs (policies, roaming, channels, security).

## Media / Conversion
- **Media converter**: converts between media types (e.g., copper ↔ fiber).

## Voice / Telephony
- **VoIP endpoint**: IP phone / softphone.
- **PBX (Private Branch Exchange)**: manages internal telephony, call routing; in VoIP often IP-PBX.

## Traffic Management
- **Load balancer**: distributes traffic across servers (L4/L7). Improves availability and scalability.

## Detection / Prevention
- **IDS (Intrusion Detection System)**: detects suspicious traffic, alerts.
- **IPS (Intrusion Prevention System)**: detects and actively blocks/drops malicious traffic.

## Intermediaries / Access Control
- **Proxy server**: intermediary for client requests (can filter, cache, log). Useful for web control and visibility.
- **RADIUS server**: central authentication/authorization/accounting (AAA), common for Wi-Fi/VPN/802.1X.
- **VPN concentrator**: terminates multiple VPN tunnels; provides remote access and site-to-site VPN.

## Security notes (why it matters)
- Each component can be an enforcement point (firewall, proxy, NAC/RADIUS) or a detection point (IDS/IPS).
- Misconfiguration risks: open management interfaces, weak AAA, poor segmentation (VLANs), exposed VPN endpoints.
