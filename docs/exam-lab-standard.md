# RHCSA Exam Lab Standard

## Purpose

This repository is focused on passing the RHCSA / EX200 exam. The labs are not designed as broad SRE, DevOps, or portfolio expansion projects unless that directly helps with the exam.

Every lab must train performance-based execution: complete the task, verify it, make it persistent where required, break something safely, fix it, and document the evidence.

## Standard lab format

Every RHCSA lab has three mandatory sections.

### Part 1 — New chapter content

This section covers the new material from the current RHCSA 10 Cert Guide chapter.

It should include:

* chapter-specific tasks
* exam-style requirements
* constraints
* verification commands
* persistence checks where relevant
* reference checks using the book, `man`, `--help`, `/usr/share/doc`, and official Red Hat documentation where useful

### Part 2 — Cumulative repetition

This section repeats all topics learned so far.

The goal is to prevent chapter isolation. The real exam will not tell you which chapter a task belongs to, so every lab after Lab 1 must mix current content with previous content.

Examples:

* Lab 2 repeats Lab 1 baseline checks plus essential tools.
* Lab 3 repeats Labs 1-2 plus file management.
* Lab 4 repeats Labs 1-3 plus text processing.
* Later labs should mix users, permissions, services, storage, SELinux, firewalld, networking, boot persistence, and troubleshooting.

### Part 3 — Break and fix

Every lab must include at least one deliberate break-and-fix exercise.

This is the most important practical training component.

Break-and-fix work must be:

* safe for a lab VM
* recoverable using RHCSA-level skills
* relevant to the current or previous topics
* verified after repair
* documented with symptom, diagnosis, fix, and verification

Examples by topic:

* wrong hostname
* broken network connection
* stopped or disabled service
* incorrect file permissions
* broken mount entry
* wrong SELinux context
* blocked firewall port
* failed SSH login
* bad cron job
* broken Apache content access
* missing package or repository issue
* boot target misconfiguration

Do not include destructive breaks that risk unrecoverable data loss unless the lab explicitly states that the VM has a snapshot or is disposable.

## What each lab must train

### 1. Speed practice

The exam is timed. Labs should gradually reduce hints and push faster execution.

### 2. Mixed objectives

RHCSA tasks are not presented chapter-by-chapter. Labs must combine objectives as the course progresses.

### 3. No-hint repetition

New content may have guidance. Repetition tasks should become increasingly direct and should not provide every command.

### 4. Reboot validation

Anything that should persist must be checked after reboot or by an equivalent persistence validation method.

### 5. Troubleshooting drills

Every lab must contain break-and-fix work. Troubleshooting should especially target boot, mounts, permissions, services, SELinux, firewalld, SSH, networking, package management, users, and scheduled tasks as those topics become available.

### 6. Man-page fluency

Labs must force use of reference material. The student should practise quickly finding syntax using `man`, `--help`, package documentation, and official documentation.

## Documentation workflow

The student performs the lab.

The assistant handles documentation.

The student sends:

* command output
* relevant notes
* errors encountered
* break-and-fix symptom, diagnosis, fix, and verification
* screenshots only if useful and non-sensitive
* answers to exactly seven reflection questions

The assistant then creates or updates the lab output file and uploads it to the correct chapter folder.

## Reflection rule

For each completed lab, ask exactly seven reflection questions.

The reflection questions should test understanding of:

* what was learned
* what was difficult
* which commands mattered
* how verification was performed
* what broke and how it was fixed
* what would fail after reboot
* what should be practised again

## Repository rule

Every generated lab must be uploaded to the correct folder:

```text
labs/<chapter-number>-<chapter-slug>/
```

Example:

```text
labs/01-installing-redhat-enterprise-linux/
```

Each lab should use clear file names such as:

```text
Lab1-Requirements.md
Lab1-Output.md
```

## Exam priority

The priority is:

```text
Pass RHCSA / EX200
```

Do not add production extensions, SRE extensions, cloud extensions, or DevOps extensions unless they directly support an exam objective.