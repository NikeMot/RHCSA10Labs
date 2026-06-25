# Commit Strategy

### Purpose

This document defines how commits should be made in this repository.

The goal is to keep the history readable, reviewable, and safe to revert.

### Commit principles

Commits should be:

* small
* logical
* complete
* descriptive
* safe to revert where possible

### When to commit

Commit when one logical unit of work is complete.

Examples:

* Create initial chapter folder structure
* Add Lab 01 requirements
* Complete Lab 01 output and evidence
* Fix a specific documentation issue
* Add a helper script for one lab

### When not to commit

Do not commit when:

* secrets or credentials are present
* unrelated changes are mixed together
* the change cannot be explained
* the repo is in a broken or confusing state
* copyrighted book files or copied course material are present

### Commit message style

Use short, descriptive messages.

Examples:

* Create RHCSA chapter folder structure
* Add Lab 01 installation requirements
* Complete Lab 01 verification evidence
* Document storage lab decisions

### Pre-commit checklist

1. Run `git status`.
2. Review unstaged changes.
3. Review staged changes with `git diff --staged`.
4. Confirm no secrets are included.
5. Confirm no private/company data is included.
6. Confirm no book PDFs, EPUBs, or copied chapters are included.
7. Confirm the commit has one clear purpose.
8. Write a meaningful commit message.

### Branching rules

Use branches when a change is risky, large, experimental, or separate from the current work on `main`.

Branch examples:

```text
docs/update-lab-template
lab/01-installing-rhel
fix/readme-structure
```

In a production or team environment, changes should normally go through pull requests before merging into `main`.