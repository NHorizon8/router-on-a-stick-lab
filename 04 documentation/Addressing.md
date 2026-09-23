

Each VLAN uses a separate /24 IPv4 subnet.

| VLAN | Department | Network | Gateway |
|------|------------|---------|---------|
| 10 | SALES | 192.168.10.0/24 | 192.168.10.1 |
| 20 | HR | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |

## Reasoning

A separate subnet is used for each VLAN because VLANs represent separate
Layer 2 networks. The router needs a Layer 3 interface in each network
in order to route traffic between them.

The /24 prefix was chosen because this is a small lab and it keeps the
addressing simple and easy to understand. Each subnet provides 254 usable
host addresses, which is more than enough for this lab.

The `.1` address is used as the default gateway for each subnet. This
makes the addressing pattern easy to recognize:

192.168.10.1 → VLAN 10 gateway
192.168.20.1 → VLAN 20 gateway
192.168.30.1 → VLAN 30 gateway