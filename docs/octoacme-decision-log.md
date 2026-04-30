# OctoAcme — Decision Log

## Purpose
Capture key decisions made during a project so that context is preserved, rationale is transparent, and decisions can be revisited efficiently if circumstances change.

## When to use
Log any decision that is:
- Non-obvious or involves trade-offs
- Cross-functional (affects more than one team or role)
- Potentially revisited later (architecture, scope, technology choice)
- Required by compliance or audit

---

## Decision Log Template

Copy and append one entry per decision. Keep entries concise.

```
### Decision [ID] — [Short Title]

- **Date:** YYYY-MM-DD
- **Status:** Proposed | Accepted | Superseded | Deprecated
- **Deciders:** [Name / Role, Name / Role, ...]
- **Context:**
  Brief description of the situation, problem, or constraint that required a decision.

- **Options Considered:**
  1. Option A — [brief description, key pros/cons]
  2. Option B — [brief description, key pros/cons]

- **Decision:**
  What was decided and why.

- **Consequences:**
  What becomes easier or harder as a result. Any follow-up actions or risks introduced.

- **Related Links:**
  - Issue / PR: [link]
  - Risk Register entry: [ID, if applicable]
```

---

## Example Entries

### Decision 001 — Use GitHub Projects for Backlog Tracking

- **Date:** 2025-01-15
- **Status:** Accepted
- **Deciders:** Project Manager, Product Manager
- **Context:**
  The team needed a lightweight project board that integrates with the existing GitHub repo without adding a new tool.

- **Options Considered:**
  1. GitHub Projects — native integration, no extra cost, limited advanced reporting
  2. Jira — richer reporting, higher admin overhead, additional cost

- **Decision:**
  Use GitHub Projects. Simplicity and native integration outweigh the reporting limitations for current team size.

- **Consequences:**
  Reporting will be done via manual markdown status updates. If the team grows beyond 10, revisit tooling.

- **Related Links:**
  - Issue: #12

---

### Decision 002 — Defer Accessibility Audit to Post-MVP

- **Date:** 2025-02-03
- **Status:** Accepted
- **Deciders:** Product Manager, UX Designer, Project Manager
- **Context:**
  Full WCAG 2.1 AA audit requires external tooling and would delay the MVP by three weeks.

- **Options Considered:**
  1. Full audit before MVP — higher quality but delayed launch
  2. Baseline keyboard nav + screen reader test only, full audit in v1.1 — faster launch with documented risk

- **Decision:**
  Proceed with baseline accessibility in MVP; schedule full audit for v1.1. UX Designer owns tracking.

- **Consequences:**
  Risk: accessibility defects may affect some users. Mitigation: prioritize issues raised post-launch. Full audit tracked as a backlog item.

- **Related Links:**
  - Risk Register entry: R-07
  - Issue: #45

---

## Notes
- Store the decision log in `docs/` or link it from the project's main README.
- Review open decisions at each sprint retrospective.
- Mark decisions as **Superseded** (not deleted) when they are replaced; preserve the history.
- See [Responsibility Map](octoacme-responsibility-map.md) for who is accountable for key decisions by lifecycle phase.
