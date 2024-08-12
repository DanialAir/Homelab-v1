# VM3: TrueNAS Configuration

## Overview

![truenas](/img/truenas.png)

This VM runs TrueNAS, an open-source storage operating system that provides network-attached storage (NAS) capabilities. TrueNAS is primarily used in this setup for VM backup storage and file network sharing. It manages these tasks with one dedicated data pool for each function. VM backups are scheduled to run automatically at 12 AM from Monday to Friday.

## Proxmox Configuration

| Resource | Configuration        |
| -------- | -------------------- |
| RAM      | 8 GB                 |
| CPU      | 4 Cores              |
| Disk     | 700 GB (on HDD)      |
| Network  | Connected to `vmbr1` |
| BIOS     | SeaBIOS              |
