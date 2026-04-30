# OctoAcme — Handoff Checklists

## Purpose
Provide lightweight, repeatable checklists for key role-to-role handoffs in the project lifecycle. Completing a handoff checklist reduces ambiguity, prevents dropped context, and gives the receiving team a clear starting point.

---

## 1. Product Manager → Delivery Team (Planning Kickoff)

**From:** Product Manager (PdM) + Business Analyst  
**To:** Project Manager + Developers + UX Designer

### Checklist
- [ ] Problem statement and goal approved by sponsor/stakeholder
- [ ] Prioritized backlog with at least one sprint's worth of estimated stories
- [ ] Acceptance criteria written for each backlog item
- [ ] Success metrics defined and measurable
- [ ] Known dependencies and integration points documented
- [ ] Initial risk list reviewed and added to Risk Register
- [ ] Stakeholder list and communication plan shared

### Handoff Artifact
Complete the [Backlog Item Template](octoacme-project-planning.md#backlog-item-template) for each story before the planning kickoff meeting.

---

## 2. Design → Engineering (Design-to-Development)

**From:** UX Designer  
**To:** Developers

### Checklist
- [ ] Final wireframes / prototypes shared in design tool (link provided)
- [ ] Component specs and annotations documented
- [ ] Accessibility requirements noted (WCAG level, keyboard nav, screen reader needs)
- [ ] Asset exports ready (icons, images, tokens)
- [ ] Design edge cases and error states covered
- [ ] Open design questions resolved or explicitly flagged for engineering decision
- [ ] Design review meeting held; Developers confirm clarity before sprint start

### Handoff Artifact
Link to design files included in each story/issue. Design review sign-off comment added to the issue before development begins.

---

## 3. Engineering → QA (Pre-QA Handoff)

**From:** Developers  
**To:** QA / testers (and Business Analyst for UAT)

### Checklist
- [ ] Feature branch merged to staging/test environment
- [ ] All acceptance criteria from the story are addressed
- [ ] Unit and integration tests written and passing in CI
- [ ] Known limitations or deviations from acceptance criteria documented in the PR/issue
- [ ] Security scanning passed (no critical or high findings unresolved)
- [ ] Setup/configuration steps for QA environment documented
- [ ] Developer available for questions during QA cycle

### Handoff Artifact
PR description includes issue link, acceptance criteria summary, test plan notes, and any known issues. QA begins only after CI is green and PR is merged to staging.

---

## 4. Release Manager — Pre-Release Gate

**From:** Engineering + QA + Security Champion  
**To:** Release Manager (for go/no-go decision)

### Checklist
- [ ] All planned acceptance criteria verified and signed off (QA/BA)
- [ ] CI pipeline passing on release branch (tests, lint, security scan)
- [ ] Security Champion sign-off on security scanning results
- [ ] Release notes drafted and reviewed by Product Manager
- [ ] Rollback plan documented and tested (or explicitly waived with justification)
- [ ] Deployment window confirmed with operations/infra
- [ ] Stakeholder announcement drafted

### Handoff Artifact
Pre-release checklist attached to the release issue/ticket. Release Manager records go/no-go decision with timestamp and rationale.

---

## 5. Release → Support & Stakeholders (Post-Deploy)

**From:** Release Manager + Product Manager  
**To:** Support team + Stakeholders

### Checklist
- [ ] Release deployed and post-deploy smoke tests passed
- [ ] Release notes published (link shared in announcement)
- [ ] Support team briefed on new features, known issues, and escalation contacts
- [ ] Monitoring dashboards updated / alerts reviewed
- [ ] Customer-facing documentation or help content updated (if needed)
- [ ] Incident response runbook updated if new systems or risks were introduced

### Handoff Artifact
Release announcement sent to stakeholder distribution list. Link to release notes and support briefing included.

---

## Notes
- Handoffs are points of high risk — incomplete handoffs are a leading cause of defects and delays.
- Any checklist item blocked or waived must be documented with a justification and owner.
- See [Responsibility Map](octoacme-responsibility-map.md) for full RACI across the lifecycle.
- See [Risk Escalation Matrix](octoacme-risk-escalation-matrix.md) for contacts when blockers arise during a handoff.
