# RHCSA Lab Environment

### Purpose

This document records the expected lab environment for the RHCSA 10 lab series.

### Recommended environment

| Component | Recommendation |
| --------- | -------------- |
| OS target | RHEL 10 preferred, CentOS Stream 10 acceptable where RHEL is unavailable |
| VMs | At least two Linux VMs: `servera` and `serverb` |
| CPU | 2 vCPU per VM where possible |
| RAM | 2 GB minimum, 4 GB preferred per VM |
| Disk | 30 GB minimum per VM, with extra disks added for storage labs |
| Network | NAT or bridged, as long as both VMs can reach each other |

### Baseline systems

| Host | Purpose |
| ---- | ------- |
| `servera.lab.local` | Primary administration target |
| `serverb.lab.local` | Remote target for SSH, file transfer, NFS, firewall, and service labs |

### Evidence expectations

Each lab should include command output or clear summaries proving that the configuration works and persists after reboot where relevant.

### Security notes

Do not commit subscription credentials, entitlement certificates, private keys, passwords, screenshots with sensitive account information, or copied copyrighted training material.