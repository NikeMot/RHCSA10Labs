# RHCSA 10 Labs

### Overview

The RHCSA10Labs repository contains hands-on Red Hat Certified System Administrator lab work based on the RHCSA 10 / EX200 learning path.

The purpose of this repository is to build practical Linux system administration competence through chapter-based labs, evidence capture, troubleshooting notes, and production-style documentation.

The labs are organised around the chapters of the RHCSA 10 Cert Guide rather than around generic infrastructure topics.

### Goals

* Build repeatable Linux administration skills through hands-on labs
* Practise RHCSA-style performance tasks on RHEL-family systems
* Document commands, decisions, evidence, mistakes, and fixes
* Develop operational judgement around persistence, security, reliability, and troubleshooting
* Produce portfolio evidence for Linux, SRE, platform, cloud, and infrastructure roles

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

### How to use this repository

Start with `labs/01-installing-redhat-enterprise-linux/` and continue in chapter order. Each lab should be completed, verified, documented, and committed before moving to the next chapter.

### Security and Privacy Notes

The repository must not contain passwords, API keys, SSH private keys, `.env` files, subscription details, company/private data, sensitive screenshots, book PDFs, EPUBs, or copied copyrighted course material.

### Status

Initial RHCSA 10 chapter-based structure created.