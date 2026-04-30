# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## UX Designer

### Role Summary
UX Designers ensure that product experiences are usable, accessible, and consistent. They translate user needs and business goals into wireframes, prototypes, and design specifications that guide engineering implementation.

### Responsibilities
- Conduct user research, usability testing, and accessibility reviews
- Create wireframes, prototypes, and design specs for engineering handoff
- Collaborate with Product Managers to refine user stories and acceptance criteria
- Maintain design consistency across features (style guide, component library)
- Review implemented features against design intent before QA sign-off

### Goals
- Deliver clear, user-centered designs that minimize rework
- Reduce ambiguity between design intent and implementation
- Ensure accessibility standards are met before release

### Typical Communication
- Design reviews with Product Manager and Developers before sprint start
- Async feedback via PR comments or design tool annotations
- Usability findings shared in sprint demos and retrospectives

### Interactions with Existing Roles
- **Product Manager**: co-creates user stories and acceptance criteria; aligns on priorities and user research findings
- **Developers**: hands off design specs and assets; provides clarifications during implementation; reviews built features
- **Project Manager**: flags design risks or scope changes that may affect timelines
- **Business Analyst**: reviews requirements together to ensure designs address documented business needs
- **Release Manager**: confirms UI changes are included in release notes and support documentation

---

## Business Analyst

### Role Summary
Business Analysts bridge product vision and technical implementation. They document detailed requirements, identify process gaps, and validate that delivered solutions meet business objectives.

### Responsibilities
- Elicit, document, and validate business and functional requirements
- Analyze upstream/downstream data and process impacts
- Create process flows, use cases, and acceptance criteria supporting PdM priorities
- Identify requirement gaps or conflicts and escalate to the Product Manager
- Support UAT (User Acceptance Testing) planning and sign-off

### Goals
- Ensure requirements are clear, complete, and testable before development begins
- Reduce defects caused by ambiguous or missing requirements
- Provide traceability from business goals to delivered features

### Typical Communication
- Requirements reviews with Product Manager and Developers before sprint planning
- Gap analysis reports and process flow documentation
- Participation in sprint reviews to validate delivered functionality

### Interactions with Existing Roles
- **Product Manager**: refines problem statements into detailed requirements; validates trade-offs
- **Project Manager**: surfaces requirement risks, dependencies, and scope changes that affect the project plan
- **Developers**: provides detailed requirements and answers technical clarification questions
- **UX Designer**: aligns on user flows and acceptance criteria to ensure designs and requirements are consistent
- **Release Manager**: provides requirement context for release notes and support documentation

---

## Release Manager

### Role Summary
Release Managers coordinate and oversee production releases from planning through post-deploy verification. They enforce deployment checklists, manage release windows, and communicate status to all stakeholders.

### Responsibilities
- Schedule and coordinate deployment windows with engineering, QA, and operations
- Verify that pre-release criteria are met (acceptance criteria, CI, security scans, rollback plans)
- Communicate release status and go/no-go decisions to stakeholders and support teams
- Maintain the release calendar and track release dependencies
- Own the rollback decision and post-release incident response coordination

### Goals
- Achieve zero-surprise deployments through thorough preparation
- Minimize production incidents caused by insufficient release readiness
- Maintain a clear, auditable release history

### Typical Communication
- Pre-release readiness reviews with Developers, QA, and PM
- Go/no-go announcements and post-deploy status updates
- Incident summary and rollback notifications when issues arise

### Interactions with Existing Roles
- **Project Manager**: aligns release windows with project milestones; escalates release-blocking risks
- **Product Manager**: confirms acceptance criteria are met before release; coordinates stakeholder announcements
- **Developers**: verifies all PRs are merged, CI passes, and rollback procedures are documented
- **UX Designer**: confirms UI/UX assets and accessibility changes are included in release scope
- **Business Analyst**: uses requirement traceability to confirm release scope matches approved requirements
- **Security Champion**: gates release on completion of security review and sign-off

---

## Security Champion

### Role Summary
Security Champions advocate for security best practices throughout the project lifecycle. They embed security thinking into design, development, and release to reduce risk and ensure compliance.

### Responsibilities
- Conduct threat modeling and security risk reviews during planning and design
- Review code changes for security vulnerabilities (OWASP top 10, secrets management, etc.)
- Ensure security scanning is configured in CI and findings are addressed before release
- Maintain and communicate the risk escalation contact matrix for security incidents
- Coordinate with the security team on vulnerability disclosure and remediation

### Goals
- Identify and mitigate security risks before they reach production
- Embed security practices into the team's standard workflow, not as a gate
- Ensure all releases pass security scanning and meet compliance requirements

### Typical Communication
- Security review sessions during sprint planning and design reviews
- Vulnerability findings reported via issues/PRs with severity and remediation guidance
- Participation in incident response for security-related production issues

### Interactions with Existing Roles
- **Project Manager**: reports high-severity security risks to the risk register; flags security items that may impact timelines
- **Product Manager**: advises on security implications of product decisions and prioritizes security-related backlog items
- **Developers**: provides guidance on secure coding practices; reviews PRs for security issues
- **Release Manager**: signs off on security scan results before release; provides go/no-go recommendation from a security standpoint
- **Business Analyst**: reviews requirements for data privacy, compliance, and security implications

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- See [Responsibility Map](octoacme-responsibility-map.md) for a RACI breakdown of key lifecycle activities across all roles.
- See [Handoff Checklists](octoacme-handoff-checklists.md) for structured handoff guidance between roles.

