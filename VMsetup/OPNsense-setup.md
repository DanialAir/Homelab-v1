# OPNsense

## Overview

![OPNsensedash](/img/OPNsensedash.png)

OPNsense is an open-source firewall and routing platform. In this home lab, OPNsense is used to manage and secure the virtual network, acting as the default gateway and DHCP server between the Proxmox VMs and the external home network. It is connected to both the virtual network (LAN) and the home network (WAN) via Proxmox's virtual bridges.

## Proxmox Configuration

| Configuration | Value         |
| ------------- | ------------- |
| **Name**      | `OPNsense`    |
| **CPU**       | 4 Cores       |
| **RAM**       | 4GB           |
| **Storage**   | 32GB (on SSD) |
| **Network**   | `vmbr0` (WAN) |
|               | `vmbr1` (LAN) |
| **BIOS**      | SeaBIOS       |

## Network Interfaces

| Interface | Bridge  | IP Address                  | Purpose               |
| --------- | ------- | --------------------------- | --------------------- |
| `vnet0`   | `vmbr0` | 192.168.68.102(DHCP)        | WAN (Home Network)    |
| `vnet1`   | `vmbr1` | 10.10.10.1(Default Gateway) | LAN (Virtual Network) |

## Additional Notes

- **Firewall Rules:** Basic rules to allow LAN to WAN traffic.
- **DHCP Server:** Enabled on LAN with a range of `10.10.10.2 - 10.10.10.250`.
- **DNS Resolver:** Configured for local DNS resolution and caching.
- **Port Forwarding:** Configured for desktop PC access to VMs.
