### Common Cisco Commands

|Command|Syntax|Purpose|
|---|---|---|
|Enable|`enable`|Enter privileged EXEC mode|
|Global configuration|`configure terminal`|Enter global configuration mode|
|Exit|`exit`|Exit the current configuration mode|
|End|`end`|Return directly to privileged EXEC mode|
|Enable interface|`no shutdown`|Enable the interface|

### R1 — Router-Specific Commands

|Command|Syntax|Purpose|
|---|---|---|
|Enter interface|`interface <interface-id>`|Enter a physical interface configuration mode|
|Create subinterface|`interface <interface-id>.<vlan-id>`|Create a router subinterface for a VLAN|
|Remove IP address|`no ip address`|Remove an IP address from an interface|
|Configure 802.1Q|`encapsulation dot1Q <vlan-id>`|Associate the subinterface with a VLAN using 802.1Q|
|Configure IPv4 address|`ip address <ip-address> <subnet-mask>`|Assign an IPv4 address to the interface|

### SW1 — Switch-Specific Commands

|Command|Syntax|Purpose|
|---|---|---|
|Create VLAN|`vlan <vlan-id>`|Create a VLAN|
|Name VLAN|`name <vlan-name>`|Assign a name to a VLAN|
|Enter interface|`interface <interface-id>`|Enter an interface configuration mode|
|Access mode|`switchport mode access`|Configure the interface as an access port|
|Assign access VLAN|`switchport access vlan <vlan-id>`|Assign an access port to a VLAN|
|Trunk mode|`switchport mode trunk`|Configure the interface as a trunk port|

### Verification Commands

| Command                   | Device   | Purpose                                        |
| ------------------------- | -------- | ---------------------------------------------- |
| `show vlan brief`         | SW1      | Display VLANs and assigned access ports        |
| `show interfaces trunk`   | SW1      | Display trunk interfaces and trunk status      |
| `show interfaces status`  | SW1      | Display the operational status of switch ports |
| `show ip interface brief` | R1       | Display interface IP addresses and status      |
| `show ip route`           | R1       | Display the IPv4 routing table                 |
| `show running-config`     | R1 / SW1 | Display the current running configuration      |