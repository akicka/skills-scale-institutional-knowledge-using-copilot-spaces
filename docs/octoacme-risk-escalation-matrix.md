# OctoAcme — Risk Escalation Contact Matrix

## Purpose
Provide a clear, role-based escalation path for risks and incidents so that issues reach the right person quickly, without ambiguity.

## When to use
- A risk in the Risk Register moves from **Low** to **Medium** or **High** impact/likelihood
- A blocker is not resolved within one standup cycle
- An incident occurs in production
- A security vulnerability is discovered

---

## Escalation Tiers

| Tier | Trigger | First Contact | Escalate To | Time Limit Before Next Tier |
|------|---------|--------------|-------------|----------------------------|
| **T1 – Team** | Blocker identified in standup; risk newly logged | Developer / Reporter | Project Manager | 1 business day |
| **T2 – Project Lead** | Unresolved T1; Medium-impact risk or dependency conflict | Project Manager | Product Manager + dependent team leads | 2 business days |
| **T3 – Sponsor** | Unresolved T2; High-impact risk; scope/budget/date at risk | Product Manager | Sponsor / Executive stakeholder | Same business day |
| **T4 – Security On-call** | Security vulnerability (High/Critical); data breach; compliance incident | Security Champion | Security On-call + Legal/Compliance (if data involved) | Immediately |

---

## Role-to-Contact Mapping

| Role | Risk/Incident Type | Primary Contact | Secondary Contact |
|------|--------------------|----------------|-------------------|
| **Developer** | Technical blocker, security finding | Project Manager | Security Champion (for security findings) |
| **UX Designer** | Design/accessibility blocker, unresolved requirements conflict | Project Manager | Product Manager |
| **Business Analyst** | Requirement conflict, missing stakeholder input | Product Manager | Project Manager |
| **Release Manager** | Release-blocking defect, failed rollback | Project Manager + Developers | Product Manager (for go/no-go) |
| **Security Champion** | High/Critical security vulnerability | Project Manager | Security On-call + Legal/Compliance |
| **Project Manager** | Cross-team dependency, budget/timeline risk | Product Manager | Sponsor |
| **Product Manager** | Scope change, strategic conflict, stakeholder alignment | Sponsor | Executive stakeholder |

---

## Severity Definitions

| Severity | Description | Response Time |
|----------|-------------|---------------|
| **Critical** | Production outage, data breach, security exploit in the wild | Immediate (< 1 hour) |
| **High** | Major feature broken, security vulnerability not yet exploited, release blocked | < 4 hours |
| **Medium** | Non-critical functionality impaired, risk materially increased | 1 business day |
| **Low** | Minor issue, risk logged but managed, no immediate impact | Next sprint/cycle |

---

## Security Incident Escalation Path

```
Reporter (Developer / Security Champion)
  └─► Security Champion (if not reporter)
        └─► Project Manager (notify immediately)
              └─► Security On-call (page or urgent Slack/email)
                    └─► Legal / Compliance (if data or regulatory impact)
                          └─► Sponsor / Executive (if breach is confirmed)
```

- Do **not** discuss unconfirmed security vulnerabilities in public channels.
- Use the security incident runbook for step-by-step response guidance.
- Log all actions taken in the incident timeline for the post-incident review.

---

## Notes
- Update this matrix at project kickoff with the actual names and contact details for each role.
- Review escalation paths at the start of each release cycle.
- See [Risk Management & Communication](octoacme-risks-and-communication.md) for the Risk Register format and communication templates.
- See [Responsibility Map](octoacme-responsibility-map.md) for role ownership across lifecycle phases.
