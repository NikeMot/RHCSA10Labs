# RHCSA Exam Lab Standard

## Purpose

This repository is focused on passing the RHCSA / EX200 exam. The labs are not designed as broad SRE, DevOps, or portfolio expansion projects unless that directly helps with the exam.

Every lab must train performance-based execution: complete the task, verify it, make it persistent where required, and document the evidence.

## Standard lab format

Every RHCSA lab has two parts.

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

Labs should include broken or ambiguous situations where appropriate, especially around boot, mounts, permissions, services, SELinux, firewalld, SSH, and networking.

### 6. Man-page fluency

Labs must force use of reference material. The student should practise quickly finding syntax using `man`, `--help`, package documentation, and official documentation.

## Documentation workflow

The student performs the lab.

The assistant handles documentation.

The student sends:

* command output
* relevant notes
* errors encountered
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
* what would fail after reboot
* what would be unsafe on the exam or in a real system
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