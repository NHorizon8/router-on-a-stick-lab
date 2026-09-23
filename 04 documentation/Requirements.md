

The lab is designed as a small office network with three separate
departments.

Each department needs its own VLAN so that the departments remain
separate Layer 2 broadcast domains.

The requirements are:

- Three VLANs for three departments
- One IPv4 subnet for each VLAN
- One Layer 2 switch for VLAN segmentation
- One router for inter-VLAN routing
- An 802.1Q trunk between the switch and router
- Router subinterfaces for the three VLAN gateways
- End devices connected to their respective VLANs

The three VLANs are:

- VLAN 10 - SALES
- VLAN 20 - HR
- VLAN 30 - IT

The design is intentionally small so that the complete Router-on-a-Stick
process can be seen clearly without adding unnecessary network devices.