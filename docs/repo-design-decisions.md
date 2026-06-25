# Repository Design Decisions

### Context

This repository contains a sequence of RHCSA 10 labs. The lab folders follow the RHCSA 10 Cert Guide chapter order rather than generic technology areas.

### Decision

Use one repository divided into numbered chapter folders under `labs/`.

### Rationale

A single repository keeps the RHCSA journey together as one connected learning path. Numbered folders make the chapter order obvious. General documentation is kept in `docs/`, while lab-specific work is kept under the relevant chapter folder.

### Alternatives considered

| Alternative | Reason not chosen |
| ----------- | ----------------- |
| One repository per chapter | Too many repositories and harder to review as one learning path |
| One flat folder | Navigation would become difficult as evidence accumulates |
| Notes only in README | README would become too long and hard to maintain |
| Private notes outside GitHub | Would not provide portfolio evidence |

### Consequences

This structure is easy to navigate, but it requires consistent naming and regular documentation discipline.

### Future changes

Additional folders may be added for mock exams, scripts, troubleshooting drills, or full-scope rebuilds.