# Ubuntu Docker Configuration

## Overview

![ubuntudocker](/img/portainer.png)
This VM hosts Docker, allowing for deployment and management of containerized applications. Portainer is used as a management tool for Docker, providing a web interface to manage Docker containers.

### Docker Containers

The following containers are deployed:

- **WireGuard**
- **Jellyfin**
- **Home Assistant**
- **Portainer**
- **AudiobookLibrary**
- **Satisfactory Server**
- **AdGuard**

## Proxmox Configuration

| Resource | Configuration        |
| -------- | -------------------- |
| RAM      | 10 GB                |
| CPU      | 4 Cores              |
| Disk     | 80 GB (on SSD)       |
| Network  | Connected to `vmbr1` |
| BIOS     | OVMF (UEFI)          |
