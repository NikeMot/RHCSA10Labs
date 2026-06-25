# RHCSA 10 Labs

### Overview

The RHCSA10Labs repository contains hands-on Red Hat Certified System Administrator lab work based on the RHCSA 10 / EX200 learning path.

The purpose of this repository is to build practical Linux system administration competence through chapter-based labs, evidence capture, troubleshooting notes, and production-style documentation.

The labs are organised around the chapters of the RHCSA 10 Cert Guide rather than around generic infrastructure topics.

### Goals

The goals of this repository are as follows:

* Build repeatable Linux administration skills through hands-on labs
* Practise RHCSA-style performance tasks on RHEL-family systems
* Document commands, decisions, evidence, mistakes, and fixes
* Develop operational judgement around persistence, security, reliability, and troubleshooting
* Produce portfolio evidence for Linux, SRE, platform, cloud, and infrastructure roles

### Skills covered

| Area | Status | Topics |
| ---- | ------ | ------ |
| Installation and lab environment | Not Started | RHEL installation, VM setup, baseline verification |
| Essential tools and files | Not Started | shell, redirection, files, archives, text tools |
| Access and identity | Not Started | SSH, users, groups, sudo, permissions |
| Networking and software | Not Started | nmcli, repositories, DNF, RPM, Flatpak |
| Operating running systems | Not Started | processes, systemd, scheduling, logging |
| Storage | Not Started | partitions, filesystems, swap, LVM |
| Boot and troubleshooting | Not Started | GRUB, targets, rescue, root password recovery |
| Automation | Not Started | Bash scripting, arguments, conditionals, loops |
| Network services and security | Not Started | SSH, Apache, SELinux, firewalld, NFS, autofs, time services |
| Final preparation | Not Started | mixed full-scope RHCSA practice |

### Repository Structure

| Path | Purpose |
| ---- | ------- |
| `docs/` | General documentation, standards, templates, decisions, and setup notes |
| `labs/` | Chapter-based RHCSA lab folders and evidence |
| `scripts/` | Helper scripts created during labs, if any |

### Lab Folder Naming

Lab folders use two-digit numbering and chapter-style slugs.

Example:

```text
labs/01-installing-redhat-enterprise-linux/
```

Each chapter folder contains a `README.md` explaining the lab focus. Lab output and evidence files should be added as the lab is completed.

### How to use this repository

Each lab should be documented with:

* Scenario
* Reference material
* Requirements
* Constraints
* Implementation tasks
* Key commands used
* Verification evidence
* Issues encountered
* Decisions made
* Security and production considerations
* Reflection questions

Start with `labs/01-installing-redhat-enterprise-linux/` and continue in chapter order.

### Security and Privacy Notes

The repository must not contain:

* Passwords
* API keys
* SSH private keys
* `.env` files
* Subscription details or entitlement credentials
* Company/private data
* Sensitive screenshots
* Book PDFs, EPUBs, or copyrighted course material
* Full copied book chapters or proprietary lab answers

### Status

Initial repository structure created. Labs will be completed chapter by chapter.