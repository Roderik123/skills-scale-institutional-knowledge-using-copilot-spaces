# OctoAcme Personas

**Updated:** Added QA Lead, Release Manager, UX Designer, Technical Writer, and On-call/Support Lead personas

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

## QA Lead

### Role Summary
QA Leads own quality assurance processes, test strategies, and release signoff. They ensure features meet quality standards before deployment and coordinate testing efforts across the team.

### Responsibilities
- Define test strategy and coverage requirements (unit, integration, e2e, smoke)
- Review and approve test plans for features
- Execute or coordinate manual testing for acceptance
- Signoff on release readiness from a quality perspective
- Maintain test environments and test data
- Track and triage bugs and quality metrics

### Goals
- Ensure high product quality and minimal production defects
- Reduce time-to-detect issues through effective test coverage
- Enable confident, fast releases through automation and clear signoff criteria

### Typical Communication / Interactions
- **With PM:** Clarify acceptance criteria, prioritize bugs, discuss feature quality vs. timeline trade-offs
- **With Product Managers (PdM):** Align on quality standards and user experience expectations
- **With Developers:** Review test coverage, collaborate on test automation, triage and reproduce bugs
- **With Release Manager:** Provide QA signoff for releases, report on test results and blockers
- **With Stakeholders:** Report quality metrics, highlight risks, and provide release confidence assessment

---

## Release Manager

### Role Summary
Release Managers coordinate and execute software releases. They ensure all pre-release requirements are met, manage deployment activities, and handle rollback procedures if needed.

### Responsibilities
- Coordinate release planning and scheduling
- Validate all pre-release checklist items are complete
- Execute or oversee deployment to staging and production
- Manage release communications and announcements
- Coordinate rollback procedures if deployments fail
- Maintain release documentation and post-mortems

### Goals
- Deliver predictable, low-risk releases
- Minimize deployment-related incidents and downtime
- Ensure clear communication to all stakeholders during releases

### Typical Communication / Interactions
- **With PM:** Align on release timelines, scope, and priorities
- **With Product Managers (PdM):** Coordinate feature releases and customer communications
- **With Developers:** Validate code freeze, coordinate hotfixes, ensure deployment readiness
- **With QA Lead:** Obtain QA signoff, review test results, coordinate smoke testing
- **With Technical Writer:** Ensure release notes and documentation are ready
- **With On-call/Support Lead:** Brief on release changes, coordinate deployment windows, prepare for potential issues
- **With Stakeholders:** Announce releases, report on deployment status

---

## UX Designer

### Role Summary
UX Designers create user-centered designs and ensure the product is intuitive, accessible, and delightful. They collaborate with Product Managers and Developers to translate user needs into design solutions.

### Responsibilities
- Conduct user research and usability testing
- Create wireframes, mockups, and prototypes
- Define interaction patterns and design systems
- Provide design specs and assets to developers
- Review implementations for design fidelity
- Signoff on UX quality before release

### Goals
- Maximize user satisfaction and product usability
- Ensure consistent, accessible user experiences
- Validate design decisions through research and testing

### Typical Communication / Interactions
- **With PM:** Collaborate on project scope and schedule
- **With Product Managers (PdM):** Understand user needs and business goals, define product vision
- **With Developers:** Provide design specs, clarify implementation details, review UI implementations
- **With QA Lead:** Collaborate on usability testing and UX bug verification
- **With Release Manager:** Provide UX signoff for releases
- **With Stakeholders:** Present design proposals and gather feedback

---

## Technical Writer

### Role Summary
Technical Writers create and maintain product documentation, including user guides, API docs, and release notes. They ensure documentation is accurate, clear, and accessible to target audiences.

### Responsibilities
- Write and maintain user-facing documentation
- Create and update API documentation and developer guides
- Draft release notes and change logs
- Review feature specs and acceptance criteria for documentation needs
- Maintain documentation site and information architecture
- Collaborate with product and engineering on content accuracy

### Goals
- Ensure users can successfully adopt and use the product
- Reduce support burden through clear, comprehensive documentation
- Maintain documentation that is current and discoverable

### Typical Communication / Interactions
- **With PM:** Understand release scope and documentation priorities
- **With Product Managers (PdM):** Align on user-facing messaging and feature positioning
- **With Developers:** Review technical accuracy, obtain code examples, clarify implementation details
- **With QA Lead:** Verify documentation against actual product behavior
- **With Release Manager:** Provide release notes and ensure documentation is ready for deployment
- **With On-call/Support Lead:** Gather feedback on common user issues to improve docs
- **With Stakeholders:** Coordinate on external communications and announcements

---

## On-call/Support Lead

### Role Summary
On-call/Support Leads manage customer-facing incidents and production issues. They triage support requests, coordinate with engineering on incident response, and ensure timely resolution of customer-impacting problems.

### Responsibilities
- Monitor production systems and respond to alerts
- Triage and prioritize customer support requests
- Coordinate incident response and escalations
- Provide feedback to product and engineering on recurring issues
- Maintain runbooks and incident playbooks
- Track support metrics and identify improvement opportunities

### Goals
- Minimize customer impact from incidents and issues
- Ensure fast, effective incident response and resolution
- Reduce recurring issues through feedback to product and engineering

### Typical Communication / Interactions
- **With PM:** Report on incident trends and prioritize fixes
- **With Product Managers (PdM):** Provide customer feedback and highlight usability issues
- **With Developers:** Escalate production issues, coordinate on debugging and hotfixes
- **With QA Lead:** Report on production bugs discovered through support channels
- **With Release Manager:** Coordinate release deployments, provide feedback on deployment-related incidents
- **With Stakeholders:** Communicate incident status and resolution timelines

---

## Usage

### How to reference these personas in other docs
- When describing a process step or responsibility, reference the relevant persona by name (e.g., "The **QA Lead** reviews the test plan...")
- Link to this document when introducing a role for the first time: `[QA Lead](octoacme-roles-and-personas.md#qa-lead)`
- Use personas in issue templates to clarify ownership (e.g., "QA Lead to provide signoff")
- In checklists, assign steps to specific personas to clarify accountability

### How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

