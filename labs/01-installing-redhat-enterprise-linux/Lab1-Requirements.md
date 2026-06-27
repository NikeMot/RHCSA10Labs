# Lab 01 — Installing Red Hat Enterprise Linux

## 1. Lab Summary

**Lab:** Lab 01 — Installing Red Hat Enterprise Linux  
**Topic area:** RHEL installation, VM build, baseline system verification, lab environment readiness  
**Difficulty:** Beginner foundation, strict evidence standard  
**Status:** Not started / In progress / Completed

### Objective

Build a clean RHCSA practice environment from scratch using two RHEL-family virtual machines. Verify that both systems are installed correctly, reachable, documented, and ready for later RHCSA labs.

This lab introduces the standard RHCSA workflow for this repository:

1. solve the lab on the systems
2. capture evidence
3. verify persistence where relevant
4. send evidence and seven reflection answers
5. allow documentation to be completed and uploaded

---

## 2. Scenario

You are preparing a controlled RHCSA / EX200 practice environment.

Before you can practise users, permissions, storage, services, SELinux, firewalld, SSH, NFS, systemd, and troubleshooting, you need two clean Linux systems with predictable names, working networking, package management visibility, enabled security controls, and documented baseline evidence.

The exam is performance-based. You are not trying to write long notes while working. You are trying to complete the task, verify it, and capture enough evidence for documentation afterwards.

---

## 3. Reference Material

Use the reference material to work out the correct steps.

| Area | Suggested reference |
| ---- | ------------------- |
| Primary book chapter | RHCSA 10 Cert Guide, Chapter 1 — Installing Red Hat Enterprise Linux |
| Exam focus | Deploy, configure, and maintain systems; operate running systems; understand and use essential tools |
| Installation docs | Official Red Hat installation documentation where needed |
| System identity | `man hostnamectl`, `man hostname` |
| Network checks | `man ip`, `man nmcli`, `man resolv.conf` |
| Storage checks | `man lsblk`, `man findmnt`, `man df`, `man swapon` |
| Service checks | `man systemctl`, `man sshd` |
| Package checks | `man dnf`, `man rpm` |
| SELinux checks | `man getenforce`, `man sestatus` |

---

## 4. Exam Lab Rule — Two Parts

Every RHCSA lab from now on has two parts.

### Part 1 — New chapter content

This section covers the current chapter content.

For Lab 01, the new content is:

* installing or preparing the RHEL-family systems
* creating the base VM environment
* setting hostnames
* verifying OS identity
* verifying storage baseline
* verifying networking baseline
* checking package management
* checking SSH, firewalld, SELinux, and the default systemd target
* proving the baseline survives reboot

### Part 2 — Cumulative repetition

This section repeats all topics learned so far.

For Lab 01, there are no previous chapters, so the cumulative section is the baseline itself:

* identify the system
* inspect users and privilege context
* inspect storage
* inspect networking
* inspect services
* inspect SELinux
* reboot and verify persistence

From Lab 02 onward, the cumulative section must include previous topics as no-hint or reduced-hint tasks.

---

## 5. What This Lab Must Train

### 1. Speed practice

Do not spend time writing the final documentation while solving the lab. Capture evidence efficiently, then documentation will be handled afterwards.

### 2. Mixed objectives

Even Lab 01 touches multiple RHCSA objective areas: installation, system identity, networking, storage inspection, service checks, SELinux checks, and reboot validation.

### 3. No-hint repetition

Use the book and system documentation. The lab gives requirements, not every command in exact order.

### 4. Reboot validation

The baseline is not complete until both systems have been rebooted and checked again.

### 5. Troubleshooting mindset

If something does not work, diagnose it. Do not skip the check. Record the issue and the fix.

### 6. Man-page fluency

Use `man`, `--help`, `/usr/share/doc`, and official docs to confirm syntax and behaviour.

---

## 6. Requirements

| ID | Requirement | Status |
| -- | ----------- | ------ |
| R1 | Create two RHEL-family virtual machines | Not started |
| R2 | Name the systems `servera.lab.local` and `serverb.lab.local` | Not started |
| R3 | Create or verify a non-root administrative user for lab work | Not started |
| R4 | Verify operating system identity and kernel information | Not started |
| R5 | Verify storage layout, mounted filesystems, and swap state | Not started |
| R6 | Verify IP configuration, default route, and DNS configuration | Not started |
| R7 | Prove both systems can communicate with each other by IP address | Not started |
| R8 | Verify package repositories or package management availability | Not started |
| R9 | Verify SSH service state | Not started |
| R10 | Verify firewalld state | Not started |
| R11 | Verify SELinux state | Not started |
| R12 | Reboot both systems and prove the baseline survives reboot | Not started |
| R13 | Capture evidence without exposing secrets or private data | Not started |

---

## 7. Constraints

You must not:

* skip verification after installation
* rely only on the GUI to prove the system state
* disable SELinux
* permanently disable firewalld
* commit passwords, SSH private keys, subscription details, or screenshots containing sensitive account information
* commit RHEL ISO files, PDFs, EPUBs, or copied book material
* proceed to Lab 02 until both systems have been reboot-tested
* mark the lab complete without command evidence

---

## 8. Expected Environment

| System | Purpose | Required hostname |
| ------ | ------- | ----------------- |
| VM 1 | Primary administration target | `servera.lab.local` |
| VM 2 | Remote target for later SSH, networking, storage, and service labs | `serverb.lab.local` |

Minimum VM guidance:

| Setting | Minimum | Preferred |
| ------- | ------- | --------- |
| CPU | 1 vCPU | 2 vCPU |
| RAM | 2 GB | 4 GB |
| Disk | 30 GB | 40 GB or more |
| Network | NAT or bridged | Same network for both VMs |
| Install type | CLI-capable server install | Minimal/server installation |

---

## 9. Part 1 — New Chapter Tasks

Complete these tasks on the two systems.

### Task 1 — Build the virtual machines

Create two RHEL-family VMs. Use RHEL 10 where possible. Use CentOS Stream 10 only if RHEL access is unavailable.

### Task 2 — Set hostnames

Configure the systems as:

```text
servera.lab.local
serverb.lab.local
```

### Task 3 — Verify administrative access

Verify that your normal lab user can log in and perform administrative work using the chosen privilege method.

Do not document passwords.

### Task 4 — Verify operating system identity

On both systems, prove:

* hostname
* operating system release
* kernel version
* architecture if useful

### Task 5 — Verify storage baseline

On both systems, prove:

* disks are visible
* filesystems are mounted
* root filesystem is present
* swap state is known
* mount layout is understood

### Task 6 — Verify networking baseline

On both systems, prove:

* IP address configuration
* default route
* DNS configuration
* NetworkManager connection state
* both machines can communicate by IP address

### Task 7 — Verify package management

Prove that package management works or clearly document why it does not.

### Task 8 — Verify services and security state

On both systems, check:

* `sshd`
* `firewalld`
* SELinux mode
* default systemd target

### Task 9 — Reboot and prove persistence

Reboot both machines and repeat the key checks.

---

## 10. Part 2 — Cumulative Repetition

For Lab 01, repeat the baseline checks without using the task descriptions above.

On both systems, produce evidence for:

| Area | Evidence expected |
| ---- | ----------------- |
| Identity | hostname, OS release, kernel |
| User context | current user, UID/GID, groups, privilege method |
| Storage | disks, filesystems, mounts, swap |
| Network | IP address, routes, DNS, NetworkManager state, ping test |
| Packages | repository or package manager status |
| Services | SSH, firewalld, default target |
| Security | SELinux mode |
| Persistence | post-reboot verification |

This is the first cumulative set. It becomes the foundation for Lab 02.

---

## 11. Evidence To Send After Solving

After you complete the lab, send command output or clear summaries for both systems.

Minimum evidence:

```bash
hostnamectl
cat /etc/os-release
uname -r
whoami
id
groups
lsblk
lsblk -f
df -h
findmnt
swapon --show
ip addr
ip route
nmcli device status
nmcli connection show
cat /etc/resolv.conf
ping -c 4 <other-server-ip>
dnf repolist
systemctl get-default
systemctl status sshd --no-pager
systemctl status firewalld --no-pager
getenforce
```

After reboot, send the key persistence checks again:

```bash
hostnamectl
ip addr
ip route
systemctl get-default
systemctl status sshd --no-pager
systemctl status firewalld --no-pager
getenforce
dnf repolist
```

---

## 12. Documentation Workflow

You solve the lab.

Documentation will be handled afterwards.

You only need to send:

* evidence output
* any issues encountered
* any decisions you made
* exactly seven reflection answers

The final `Lab1-Output.md` will be created and uploaded to this folder.

---

## 13. Seven Reflection Questions

Answer these after completing the lab.

1. What was the most important thing you learned while building the two RHEL-family systems?
2. Which part of the lab was hardest or slowest?
3. Which command helped you the most, and why?
4. What evidence proves that both systems are ready for the next lab?
5. What would break later if you skipped the reboot verification?
6. Which part of the baseline are you least confident about?
7. What will you practise again before starting Lab 02?

---

## 14. Completion Criteria

Lab 01 is complete only when:

* both systems boot successfully
* both hostnames are correct
* administrative access is verified
* storage baseline is known
* networking baseline is known
* both systems can communicate by IP address
* package manager state is known
* SSH state is known
* firewalld state is known
* SELinux state is known
* key checks have been repeated after reboot
* evidence is captured
* seven reflection questions are answered
* final documentation is uploaded to GitHub
