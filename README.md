# Home SOC Lab — Network Topology

## Overview
Designed and configured a virtual cybersecurity lab network using Oracle VirtualBox. The topology separates internet access, private virtual-machine communication, and host-to-VM connectivity.

## Lab Environment
- Parrot Security OS
- Kali Linux
- Ubuntu Server
- Windows Server 2022 (`DC01`)
- Oracle VirtualBox

## Network Architecture
Three virtual networking modes are used:

- **NAT:** Provides outbound internet connectivity.
- **Internal Network (`SOC-INTERNAL`):** Enables private communication between lab VMs using `10.10.20.0/24`.
- **Host-Only:** Enables communication between the Windows host and lab VMs using `192.168.220.0/24`.

## Internal Network IP Addressing

| Virtual Machine | IPv4 Address |
|---|---|
| Parrot Security | `10.10.20.10/24` |
| Kali Linux | `10.10.20.20/24` |
| Ubuntu Server | `10.10.20.40/24` |
| Windows Server 2022 | `10.10.20.50/24` |

## Validation
- Configured persistent Internal Network IP addresses on Parrot Security and Kali Linux.
- Verified Parrot's Internal Network IP remained assigned after reboot.
- Successfully tested connectivity from Windows Server to Parrot, Kali, and Ubuntu using ping.

## Documentation
See `Documentation/Home-Lab-Topology.md` for the complete network design, IP allocation, configuration details, and connectivity results.

## Purpose
This lab provides a foundation for future cybersecurity exercises, network monitoring, server administration, and Active Directory practice.
