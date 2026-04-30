# OctoAcme — Responsibility Map (RACI)

## Purpose
Provide a single-page reference showing who is **Responsible**, **Accountable**, **Consulted**, or **Informed** for key activities across the project lifecycle. Use this table to reduce ambiguity during planning and handoffs.

## RACI Key
| Code | Meaning |
|------|---------|
| **R** | Responsible — does the work |
| **A** | Accountable — owns the outcome; one per activity |
| **C** | Consulted — provides input before the activity completes |
| **I** | Informed — notified when the activity is complete |

---

## Lifecycle Responsibility Map

| Activity | Project Manager | Product Manager | Developer | UX Designer | Business Analyst | Release Manager | Security Champion |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **Initiation** | | | | | | | |
| Define problem statement & goals | C | **A/R** | I | I | C | I | I |
| Identify stakeholders & champions | **A/R** | C | I | I | C | I | I |
| Create project one-pager | **R** | **A** | I | I | C | I | I |
| Initial risk identification | **A/R** | C | C | I | C | I | C |
| Go/no-go decision | **R** | **A** | I | I | I | I | I |
| **Planning** | | | | | | | |
| Backlog creation & prioritization | C | **A/R** | C | C | **R** | I | I |
| Acceptance criteria definition | C | **A** | C | C | **R** | I | I |
| UX design & prototype | I | C | C | **A/R** | I | I | I |
| Threat modeling / security review | C | I | C | I | I | I | **A/R** |
| Release plan & milestone map | **A/R** | C | C | I | I | C | I |
| Definition of Done | **R** | **A** | C | C | C | I | C |
| **Execution** | | | | | | | |
| Sprint planning facilitation | **A/R** | C | C | C | C | I | I |
| Feature implementation | I | I | **A/R** | I | I | I | C |
| Code review & PR approval | I | I | **A/R** | I | I | I | C |
| Security scanning & remediation | I | I | **R** | I | I | I | **A** |
| Design QA (implementation vs. spec) | I | C | R | **A/R** | I | I | I |
| Requirements validation / UAT | I | **A** | C | I | **R** | I | I |
| Risk register updates | **A/R** | C | C | I | C | I | C |
| **Release** | | | | | | | |
| Pre-release readiness review | C | C | R | I | C | **A/R** | C |
| Security sign-off | I | I | C | I | I | C | **A/R** |
| Go/no-go decision | C | C | I | I | I | **A** | C |
| Deployment execution | I | I | **R** | I | I | **A** | I |
| Stakeholder announcement | C | **A/R** | I | I | I | C | I |
| Release notes | I | C | R | I | C | **A/R** | I |
| **Retrospective** | | | | | | | |
| Retrospective facilitation | **A/R** | C | C | C | C | C | C |
| Action item ownership assignment | **A/R** | C | C | C | C | C | C |
| Improvement backlog updates | C | **A** | C | C | C | C | C |

---

## Notes
- One **A** (Accountable) per row — if two roles share accountability, clarify ownership before the activity starts.
- **C** (Consulted) roles should be engaged before the activity is finalized, not after.
- Update this map at project kickoff to reflect the actual team composition.
- See [Roles & Personas](octoacme-roles-and-personas.md) for full role descriptions.
- See [Handoff Checklists](octoacme-handoff-checklists.md) for structured transition guidance between key handoff points.
