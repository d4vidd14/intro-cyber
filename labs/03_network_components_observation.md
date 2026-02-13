# Lab: Observing network components from a host

## 1) Identify default gateway (router)
- Windows:
  ipconfig
- Linux:
  ip r

## 2) See ARP/neighbor table (switch/L2 context)
- Windows:
  arp -a
- Linux:
  ip neigh

## 3) Quick connectivity + ICMP
ping -c 3 1.1.1.1   # Linux
# Windows:
ping 1.1.1.1

## 4) (Optional) Trace route (routers hops)
- Windows:
  tracert 1.1.1.1
- Linux:
  traceroute 1.1.1.1
