**==Note : For best experiance open file in obsidian==**

![[topology image.png]]

# Router-on-a-Stick Lab

This project is a small office network built to demonstrate inter-VLAN
routing using Router-on-a-Stick.

The network has three departments:

- VLAN 10 - SALES
- VLAN 20 - HR
- VLAN 30 - IT

Each department is placed in a separate VLAN and IPv4 subnet. A single
router interface is used as a trunk connection to the switch, with
separate router subinterfaces providing the default gateway for each VLAN.

The main purpose of the lab is to understand how traffic moves between
different VLANs through a router using 802.1Q trunking.

## Topology

The Packet Tracer topology is available in:

`topology/router-on-a-stick.pkt`

The network consists of:

- R1 - Router
- SW1 - Access Switch
- PC1 - SALES
- PC2 - HR
- PC3 - IT

The link between R1 and SW1 is an 802.1Q trunk.

## VLANs

| VLAN | Department | Network         |
| ---- | ---------- | --------------- |
| 10   | SALES      | 192.168.10.0/24 |
| 20   | HR         | 192.168.20.0/24 |
| 30   | IT         | 192.168.30.0/24 |

R1 provides the gateway for all three networks.

## Configuration

The device configurations are available in:

- `configs/R1.txt`
- `configs/SW1.txt`

The reasoning behind the network design and addressing is documented
under `documentation/`.

## Lab Goal

After configuration, devices in different VLANs should be able to
communicate through R1.

---


